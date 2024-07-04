# Use-ros1_bridge-to-print-topic-from-ros1-to-ros2-

mkdir -p ~/ros1_bridge_ws/src 

cd ~/ros1_bridge_ws/src 

<img width="1022" alt="‏لقطة الشاشة ١٤٤٥-١٢-٢٨ في ٥ ٤٢ ٤٦ م" src="https://github.com/ijana7/Use-ros1_bridge-to-print-topic-from-ros1-to-ros2-/assets/173642526/0e1a13ba-f120-419c-9d17-6a0c6a9519c6">

git clone -b foxy https://github.com/ros2/ros1_bridge.git 

<img width="1710" alt="‏لقطة الشاشة ١٤٤٥-١٢-٢٧ في ١١ ٠١ ١٥ م" src="https://github.com/ijana7/Use-ros1_bridge-to-print-topic-from-ros1-to-ros2-/assets/173642526/10864d11-e8c4-4858-8b40-626b4a2e8d24">

source ~/catkin_ws/devel/setup.bash

source ~/ros2_ws/install/setup.bash

olcon build --packages-select ros1_bridge --cmake-force-configure --cmake-args -DBUILD_TESTING=FALSE 

<img width="1710" alt="‏لقطة الشاشة ١٤٤٥-١٢-٢٧ في ١١ ٠٩ ٣١ م" src="https://github.com/ijana7/Use-ros1_bridge-to-print-topic-from-ros1-to-ros2-/assets/173642526/b53007bb-6e44-4cc6-a2fe-4d8de8bee4d6">
ros2 run ros1_bridge dynamic_bridge --print-pairs 

<img width="1710" alt="‏لقطة الشاشة ١٤٤٥-١٢-٢٧ في ١١ ١١ ٠٨ م" src="https://github.com/ijana7/Use-ros1_bridge-to-print-topic-from-ros1-to-ros2-/assets/173642526/24a6ca65-1370-406b-8689-241d72351677">

<img width="1710" alt="‏لقطة الشاشة ١٤٤٥-١٢-٢٧ في ١١ ١٢ ٣٢ م" src="https://github.com/ijana7/Use-ros1_bridge-to-print-topic-from-ros1-to-ros2-/assets/173642526/1edc823f-3fcf-4c5c-9976-2dcaf5244870">
os2 topic echo /joint_states sensor_msgs/msg/JointState
<img width="1710" alt="‏لقطة الشاشة ١٤٤٥-١٢-٢٧ في ١١ ٣٣ ٥٤ م" src="https://github.com/ijana7/Use-ros1_bridge-to-print-topic-from-ros1-to-ros2-/assets/173642526/0f689cbc-fc5e-4ebb-9cde-38e09f9334dc">

