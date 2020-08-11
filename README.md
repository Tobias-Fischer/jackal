jackal
======

Common packages for Jackal, including messages and robot description. These are packages relevant
to all Jackal workspaces, whether simulation, desktop, or on the robot's own headless PC.


QUT10
======

Changes:
- Use TEB local planner, works much better than default
- Provide move_base map with `map_added_obstacles` to be avoided (helpful with manually overlaid obstacles, e.g. the glass walls in S11)
- Fix IMU: Use `imu_bias_remover` as otherwise drift happens when robot is static
- Fix IMU: Only use IMU to provide yaw velocity values and ignore other values in `robot_localization`
- More sensible acceleration values
- Use front+back+velodyne laser scans as observation sources for obstacle avoidance
- Increase inflation layer so robot stops hugging walls when turning
