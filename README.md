# robot-butler
This project involves the development of a robot butler for the French Door Cafe using ROS2. The robot is designed to autonomously handle food delivery tasks based on orders received by the host. It follows a series of steps to navigate between its home position, the kitchen, and customer tables. 
 Autonomous Navigation: Moving to designated locations without manual intervention.
 Task Confirmation: Waiting for confirmation at the kitchen or customer table before proceeding.
 Timeout Management: Returning to the home position after completing tasks or if a timeout occurs due to lack of confirmation.
 
Workspace Setup
create a new ROS2 workspace:
mkdir -p ros2_ws/src
cd ros2_ws
Clone the repository:
git clone https://github.com/SANJAYKRISHNAP/robot-butler.git

Build the workspace:
colcon build

Source the workspace:
source ./install/setup.sh

Running Nodes and Launch Files
Run the primary ROS2 node:
ros2 run robot_butler robot_butler_node

Publish to topics:
Send an order message to the order topic:
ros2 topic pub /order_topic std_msgs/msg/String "data: '1'"

Publish a confirmation message to the confirmation topic:
ros2 topic pub /confirmation_topic std_msgs/msg/String "data: 'Order confirmed'"
