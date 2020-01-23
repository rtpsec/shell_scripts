time_since_reboot_seconds="$(awk '{print $1}' /proc/uptime)" # / 86400 |bc
seconds_in_day="86400"
time_since_reboot_days=$( echo "$time_since_reboot_seconds / $seconds_in_day" |bc  )
number_of_days="90"

fun_check_uptime() {

if [ $time_since_reboot_days -ge $number_of_days ]; then
        echo "It's time for a reboot"
        # insert logic here if its online for more than 90 days
else
        echo $time_since_reboot_days
        # It wasn't online for more than the number of days
fi

}

fun_check_uptime
