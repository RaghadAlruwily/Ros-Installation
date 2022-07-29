# Ros-Installation
How to install ros subsystem on ubuntu system  (you may need virtual environment to get ubuntu system) :

1-	Open terminal on ubuntu 
2-	Write in terminal :
•	sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' 
(you may need to write the password which is your password )

•	sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

•	and then to update system :
sudo apt-get update

•	sudo apt-get install ros-kinetic-desktop-full 
this instruction take long time to finish( if you get an error in this instruction you can rewrite the instruction )

•	apt-cache search ros-kinetic

•	echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc


•	source ~/.bashrc

•	sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

•	sudo apt install python-rosdep

•	sudo rosdep init

•	rosdep update

•	to install catkin workspace : 

sudo apt-get install ros-noetic-catkin

•	mkdir -p ~/catkin_ws/src 
( note: catkin_ws where is the name of workspace folder, you can change it as you want )

•	cd ~/catkin_ws/

•	catkin_make

•	now wil install arm machin package in catkin_ws folder:

cd ~/catkin_ws/src

•	git clone https://github.com/smart-methods/arduino_robot_arm.git

•	cd ~/catkin_ws

•	rosdep install --from-paths src --ignore-src -r -y

•	sudo apt-get install ros-kinetic-moveit

•	sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

•	sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

•	sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

•	sudo nano ~/.bashrc

•	at the end of the (bashrc) file add the follwing line:
       source /home/raghadkr/catkin_ws/devel/setup.bash  
(note: raghadkr is my username, you must change it to your username in ubuntu system, you cane get the same path from: 1- enter catkin_ws folder 2- select and right click on setup.bash file 3- go to properties 4- copy path location)
save file and exit
•	again in terminal :
-	source ~/.bashrc
-	roslaunch robot_arm_pkg check_motors.launch

and here the ros system with arm machine package going to open

![Screenshot (49)](https://user-images.githubusercontent.com/100563503/181785051-e8358069-8595-41d3-a25e-82bb54a48445.png)
