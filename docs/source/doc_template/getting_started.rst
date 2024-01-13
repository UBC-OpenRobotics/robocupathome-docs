.. _getting-started:

Getting Started
===============

This section provides basic instructions to get SimpleBot up and running. 
This page should answer basic questions such as

1. What are the basic launch files and what are they for?
2. What are the arguements that can be passed to the launch files? 
3. What environment variables does launching require?

A block diagram of the system would be helpful here. 

If you have any machine learning models you used. include locations of the model files here as well.

.. _launch-files:

1. Launch the SimpleBot::

    roslaunch simplebot bringup.launch

2. The robot should now be operational and responding to simple navigation
commands and performing basic object detection.

arguements
----------
**simulation:** (default: false) If true, the robot will be launched in simulation mode. If false, the robot will be launched look for hardware drivers to launch in real mode.

