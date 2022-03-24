init_notice="$(curl https://www.tuiost.edu.np/ | grep 'b class' | cut -d '>' -f 2 | cut -d '<' -f 1 | head -n4)"
sleep 10s
notify-send scriptstart 'scriptisrunning'

while true 
do
sleep 20m
final_notice="$(curl https://www.tuiost.edu.np/ | grep 'b class' | cut -d '>' -f 2 | cut -d '<' -f 1 | head -n4)"

if [[ $init_notice != $final_notice ]]
then 
	notify-send TU-NOTICE "$final_notice"
	aplay ~/notify.wav
	init_notice=$final_notice
else
	echo same

fi
done

