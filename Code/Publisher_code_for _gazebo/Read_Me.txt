Mavros installation

1.Run this -> sudo apt-get install ros-kinetic-mavros ros-kinetic-mavros-extras

2. source this-> wget https://raw.githubusercontent.com/mavlink/mavros/master/mavros/scripts/install_geographiclib_datasets.sh
./install_geographiclib_datasets.sh

3.For initiating mavros to px4 connection roslaunch mavros px4.launch fcu_url:="udp://:14540@192.168.1.36:14557"


For PX4

1.Download  and source this script ->https://raw.githubusercontent.com/PX4/Devguide/v1.8.0/build_scripts/ubuntu_sim_ros_gazebo.sh

2.git clone https://github.com/PX4/Firmware.git

3.To launch PX4->       cd <Firmware_clone>
			make posix_sitl_default gazebo
			source ~/catkin_ws/devel/setup.bash    // (optional)
			source Tools/setup_gazebo.bash $(pwd) $(pwd)/build/posix_sitl_default
			export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)
			export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)/Tools/sitl_gazebo
			roslaunch px4 posix_sitl.launch

Create a ROS package and run this python file missionfly2.py




