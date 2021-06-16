\# cat /usr/lib/udev/kdump-udev-throttler <br>
\#!/bin/bash <br>
\# This util helps to reduce the workload of kdump service restarting <br>
\# on udev event. When hotplugging memory / CPU, multiple udev <br>
\# events may be triggered concurrently, and obviously, we don't want <br>
\# to restart kdump service for each event. <br>

\# This script will be called by udev, and make sure kdump service is <br>
\# restart after all events we are watching are settled. <br>

\# On each call, this script will update try to aquire the $throttle_lock <br>
\# The first instance acquired the file lock will keep waiting for events <br>
\# to settle and then reload kdump. Other instances will just exit <br>
\# In this way, we can make sure kdump service is restarted immediately <br>
\# and for exactly once after udev events are settled. <br>

throttle_lock="/var/lock/kdump-udev-throttle" <br>

exec 9>$throttle_lock <br>
if [ $? -ne 0 ]; then <br>
        echo "Failed to create the lock file! Fallback to non-throttled kdump service restart" <br>
        /bin/kdumpctl reload <br>
        exit 1 <br>
fi <br>

flock -n 9 <br>
if [ $? -ne 0 ]; then <br>
        echo "Throttling kdump restart for concurrent udev event" <br>
        exit 0 <br>
fi <br>

\# Wait for at least 1 second, at most 4 seconds for udev to settle <br>
\# Idealy we will have a less than 1 second lag between udev events settle <br>
\# and kdump reload <br>
sleep 1 && udevadm settle --timeout 3 <br>

\# Release the lock, /bin/kdumpctl will block and make the process <br>
\# holding two locks at the same time and we might miss some events <br>
exec 9>&- <br>

/bin/kdumpctl reload <br>

exit 0 <br>
