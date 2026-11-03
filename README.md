# 4231_Group_Project

## Installation
### Realsense Camera
```bash
sudo apt install ros-humble-librealsense2*
```

### Moveit
```bash
sudo apt install ros-humble-moveit
```

### UR Driver
```bash
sudo apt-get install ros-humble-ur
```

### USB Camera
```bash
  sudo apt install ros-humble-v4l2-camera
```

## Running Code
### Bringup
- **Game pipeline on the real arm** (marker, `dock_node`, `manager_node`): `docs/dress_rehearsal.md`.
- **Models, simulation, staged real docking** (`wire_description`, `wire_trace`): `docs/sim_and_real_docking.md`.
- What was added and which existing files changed: `docs/MERGE_NOTES.md`.

Every terminal, from the workspace root:
```bash
cd ~/4231_Group_Project/proj_ws && source install/setup.bash
```
Build from the workspace root only (`proj_ws`), once after pulling: `colcon build --symlink-install`.

### Realsense Camera
```bash
ros2 launch realsense2_camera rs_launch.py pointcloud.enable:=true
```