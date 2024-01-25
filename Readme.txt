To launch Lio sam: 
roslaunch lio_sam run.launch

Play the existing Bag file by author, linked in the git repo of the publisher:
rosbag play park_dataset.bag -r 3

While playing the rosbag use the following command:
rosbag play morning_stereo_rgb_ir_lidar_gps.bag /ns1/velodyne_points:=points_raw imu/imu:=imu_raw

To save the PCD maps created by the algorithm:
rosservice call /lio_sam/save_map 0.2 "/Downloads/LOAM/"
