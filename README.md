# Dynamixel_SETUP
sudo apt update
sudo apt install ros-<your-ros-distro>-dynamixel-sdk
sudo apt install ros-<your-ros-distro>-dynamixel-workbench

sudo chmod 777 /dev/ttyUSB0

Change the content in ~/dynamixel_workbench_controllers/config/basic.config

roslaunch dynamixel_workbench_controllers dynamixel_controllers.launch
rosservice call /dynamixel_workbench/dynamixel_command "command: ''
id: 1
addr_name: 'Goal_Position'
value: 2048"

Then the motor will rotate, in which the value range is (0,4096)
