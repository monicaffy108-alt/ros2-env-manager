# ROS2 Environment Manager

> A TRAE Skill for diagnosing and managing ROS2 environments on Windows and WSL.

## What It Does

This skill helps you:

- **Check ROS2 installation status** on Windows and WSL
- **Compare ROS2 versions** (Humble, Jazzy, Rolling, etc.)
- **Get installation guidance** for your platform
- **Troubleshoot** common ROS2 environment issues

## ROS2 Version Reference

| Version | Type | Support Period | Ubuntu |
|---------|------|----------------|--------|
| Humble Hawksbill | LTS (5 years) | 2022 - 2027 | 22.04 |
| Iron Irwini | Regular | 2023 - 2024 | 22.04 |
| Jazzy Jalisco | LTS (3 years) | 2024 - 2027 | 24.04 |
| Rolling Ridley | Rolling dev | Continuous | Latest |

### Which version should I choose?

| Scenario | Recommended |
|----------|-------------|
| Beginner / Production / Need stability | **Humble** |
| Want newer features, still stable | **Jazzy** |
| Developer / Test latest features | **Rolling** |

## What It Checks

| Check Item | Windows | WSL |
|------------|---------|-----|
| Environment variables (`ROS_DISTRO`, etc.) | ✅ | ✅ |
| Installation paths (`C:\dev\ros2_*`, `/opt/ros/`) | ✅ | ✅ |
| `ros2` command availability | ✅ | ✅ |
| Python `rclpy` module | ✅ | ✅ |
| `colcon` / `ament` build tools | ✅ | ✅ |

## Common Issues & Solutions

| Problem | Cause | Fix |
|---------|-------|-----|
| `ros2` command not found | Not in PATH or setup script not run | Run `setup.bat` (Windows) or `source /opt/ros/<distro>/setup.bash` (WSL) |
| `rclpy` import error | Python env not configured | Reinstall ROS2 or check Python version compatibility |
| No ROS2 in WSL | ROS2 not installed in WSL | Install separately inside WSL (independent from Windows) |

## File Structure

```
ros2-env-manager/
├── README.md      # This file
└── SKILL.md       # Skill definition for TRAE
```

## How to Use

1. Install this skill in your TRAE workspace under `.trae/skills/`
2. Ask TRAE questions like:
   - "检查我的ROS2环境"
   - "Humble和Jazzy有什么区别？"
   - "WSL里怎么装ROS2？"

## License

MIT
