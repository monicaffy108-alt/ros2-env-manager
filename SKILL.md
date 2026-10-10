---
name: "ros2-env-manager"
description: "Diagnoses and manages ROS2 environments on Windows and WSL. Invoke when user asks about ROS2 installation status, version comparisons, environment setup, or troubleshooting ROS2 issues."
---

# ROS2 环境管理

## 触发条件
当用户询问以下话题时激活：
- ROS2是否已安装 / 检查ROS2环境
- ROS2版本区别（Humble/Jazzy/Rolling等）
- ROS2安装建议
- ROS2环境变量问题
- WSL中的ROS2状态

## 核心能力

### 1. 环境检查
检查以下位置：
- Windows环境变量：`ROS_DISTRO`, `AMENT_PREFIX_PATH`, `ROS_VERSION`
- 常见安装路径：`C:\dev\ros2_*`, `C:\opt\ros\*`, `C:\ros2`
- `ros2` 命令是否可用
- Python `rclpy` 模块是否安装
- `colcon` / `ament` 构建工具
- WSL中的ROS2安装（`/opt/ros/`）

### 2. 版本知识
ROS2版本按字母表顺序命名（形容词 + 龟/爬行动物）：

| 版本 | 类型 | 支持周期 | 对应Ubuntu |
|------|------|---------|-----------|
| Humble Hawksbill | LTS (5年) | 2022-2027 | 22.04 |
| Iron Irwini | 普通 | 2023-2024 | 22.04 |
| Jazzy Jalisco | LTS (3年) | 2024-2027 | 24.04 |
| Rolling Ridley | 滚动开发版 | 永久更新 | 最新版 |

**版本选择建议**：
- 初学者/生产环境/求稳定 → **Humble**（教程最多）
- 要较新特性但仍要稳定 → **Jazzy**
- 开发者/测试最新功能 → **Rolling**

### 3. 安装路径
- Windows：通常装在 `C:\dev\ros2_humble` 或 `C:\opt\ros\humble\x64`
- WSL Ubuntu：安装在 `/opt/ros/humble/`
- 安装后需运行 `setup.bat` (Windows) 或 `source /opt/ros/humble/setup.bash` (WSL)

### 4. 常见问题
- `ros2` 命令不可用 → 未添加到PATH或未运行setup脚本
- `rclpy` 找不到 → Python环境未配置或ROS2未正确安装
- WSL中无ROS2 → 需在WSL内单独安装，与Windows不互通
