## RESEARCHTRACK1-ASSIGNMENT-3
## OBJECTIVE
This assignment is a C++ program describes the robot executing on the behaviours listed below.

Autonomously reach a User entering Co-ordinates X and Y.

Control or Move the robot using keyboard keys.

## HOW IT WORKS
At first, we launch the simlation_gmapping.launch file which opensup the robot in RVIZ and robot world (map) in gazebo respectively.

second, the move_base package requires to send the goal to the topic move_base/goal by sending the message type move_base_msgs/MoveBaseActionGoal, and by same we do for feedback and current goal also. For this we launch the move_base.launch file.

And at the last,  we have the robot.cpp file where 3 publishers and subscribers are declared position of the goal, goal coordinates and laser scanner for manual driving assistance respectively. All these subscribers are run simultaneously by multithreading concept.

## So by these the robot can: 
 1.Reach the goal autonomously -User enters the x and y coordinates where the robot should go. Publishes the goal enters to move_base/goal. 
 2.User control using keybaord -User can control the robot using the list of commands (keyboard keys) and move accordingly.

## INSTRUCTIONS TO RUN THE CODE
Step 1 : Open the terminal and go to src of your ROS workspace and clone the package

<pre><code>https://github.com/santhoshsanty308/Rt1.git</code></pre>

Step 2 : Now to build your clonned code run the command - 

<pre><code>catkin_make</code></pre>
catkin_make
step 3 : Open a each new terminal for the following commands seperately -

Terminal-1.

<pre><code>roslaunch third_assignment simulation_gmapping.launch</code></pre>

Terminal-2.

<pre><code>roslaunch third_assignment move_base.launch</code></pre>

Terminal-3.

<pre><code>rosrun third_assignment finalrobot</code></pre>
