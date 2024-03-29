.. sectnum::
    :depth: 3

=======================
pointcloud_to_laserscan
=======================

.. note:: 

   This page is meant to be used as an **example** for how simple packages should be documented for this readthedocs for UBC Open Robotics by using the existing package: 
   `pointcloud_to_laserscan`. The Ros wiki for this package can be found `here <http://wiki.ros.org/pointcloud_to_laserscan>`_.
   
This package contains a single node, `pointcloud_to_laserscan`, which converts a 3D Point Cloud into a 
2D laser scan. This is useful for making devices like the Kinect appear like a laser scanner for 
2D-based algorithms (e.g. laser-based SLAM). 

* Maintainer status: maintained
* Maintainer: Paul Bovbel <paul AT bovbel DOT com>, Michel Hidalgo <michel AT ekumenlabs DOT com>
* Author: Paul Bovbel <paul AT bovbel DOT com>, Tully Foote
* License: BSD
* Bug / feature tracker: https://github.com/ros-perception/perception_pcl/issues
* Source: git https://github.com/ros-perception/pointcloud_to_laserscan.git (branch: lunar-devel)

Node
===========

pointcloud_to_laserscan_node
----------------------------

pointcloud_to_laserscan_node takes a point cloud and generates a 2D laser scan based on the provided parameters.

Subscribed Topics
^^^^^^^^^^^^^^^^^

``cloud_in`` (`sensor_msgs/PointCloud2 <http://docs.ros.org/en/api/sensor_msgs/html/msg/PointCloud2.html>`_.)
    The input point cloud.

Published Topics
^^^^^^^^^^^^^^^^
``scan`` (`sensor_msgs/LaserScan <http://docs.ros.org/en/api/sensor_msgs/html/msg/LaserScan.html>`_.)
    The output laser scan.

Parameters
^^^^^^^^^^

``~min_height`` (``double``, default: 0.0)
    The minimum height to sample in the point cloud in meters.
``~max_height`` (``double``, default: 1.0)
    The maximum height to sample in the point cloud in meters.
``~angle_min`` (``double``, default: -π/2)
    The minimum scan angle in radians.
``~angle_max`` (``double``, default: π/2)
    The maximum scan angle in radians.
``~angle_increment`` (``double``, default: π/360)
    Resolution of laser scan in radians per ray.
``~scan_time`` (``double``, default: 1.0/30.0)
    The scan rate in seconds.
``~range_min`` (``double``, default: 0.45)
    The minimum ranges to return in meters.
``~range_max`` (``double``, default: 4.0)
    The maximum ranges to return in meters.
``~target_frame`` (``str``, default: none)
    If provided, transform the pointcloud into this frame before converting to a laser scan. Otherwise, laser scan will be generated in the same frame as the input point cloud.
``~concurrency_level`` (``int``, default: 1)
    Number of threads to use for processing pointclouds. If 0, automatically detect number of cores and use the equivalent number of threads. Input queue size for pointclouds is tied to this parameter. In nodelet form, number of threads is capped by the nodelet manager configuration.
``~use_inf`` (``boolean``, default: true)
    If disabled, report infinite range (no obstacle) as range_max + 1. Otherwise report infinite range as +inf. Associated with the inf_is_valid parameter for costmap_2d obstacle layers.

Nodelet
=======
Same API as node, available as pointcloud_to_laserscan/pointcloud_to_laserscan_nodelet.