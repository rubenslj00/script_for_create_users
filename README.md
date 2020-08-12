# script_for_create_users

#!/bin/bash

function run() {
for user in $NAME;
do
	sudo adduser $NAME
	home="/home/$NAME"
	sudo mkdir /home/$NAME/.ssh
	sudo cp /home/ubuntu/publickey.txt /home/$NAME/.ssh/authorized_keys
done
}

for i in {1..5};
do
	echo "Enter your name: "
	read NAME
	run
done
