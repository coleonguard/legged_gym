# Tasks Done
 - Terrain Flat - just changed it to 'plane' setting which sets all z coordinates to zero in legged_robot.py
 - Velocity Goal & 1D Direction - set curriculum to False in legged_robot_config/.../commands class. For phase 2 training, set to True.
    - False restricts the values to the ones in the lin_vel_... arrays in ranges class. So I restricted the array to just .1 m/s (.5-.6) for now just to learn it quickly for phase 1.
    - true expands the ranges when the reward from actions passes 80% max, which is just a better version of phase 2 training, so just set curriculum to True for that and expand the range using max_curriculum, maybe modifying the step size in update_command_curriculum to more slowly expand for curriculum learning.
    - Set y-axis movement to zero with no range.