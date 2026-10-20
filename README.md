<div align="center">

# 🤖 ROS2 Environment Manager

> **一键诊断 & 管理你的 ROS2 环境**
>
> _A TRAE Skill for diagnosing and managing ROS2 environments on Windows & WSL_

[![ROS2](https://img.shields.io/badge/ROS2-Humble%20%7C%20Jazzy%20%7C%20Rolling-blue?style=for-the-badge&logo=ros)](https://docs.ros.org/)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20WSL%20%7C%20Linux-green?style=for-the-badge&logo=windows)](https://github.com/monicaffy108-alt/ros2-env-manager)
[![TRAE Skill](https://img.shields.io/badge/TRAE-Skill-orange?style=for-the-badge)](https://github.com/monicaffy108-alt)
[![License](https://img.shields.io/github/license/monicaffy108-alt/ros2-env-manager?style=for-the-badge)](LICENSE)

[English](#-what-it-does) · [中文说明](#-功能介绍)

</div>

---

## ✨ What It Does

This skill helps you quickly diagnose and manage ROS2 environments without the hassle of manual checking. Perfect for both beginners and experienced ROS developers.

| | Feature | Description |
|---|---|---|
| 🔍 | **Environment Check** | Scan ROS2 installation status on Windows & WSL in one go |
| 📊 | **Version Compare** | Humble vs Jazzy vs Rolling — know which one fits you best |
| 🛠️ | **Troubleshooting** | Common issues? Get instant solutions and fix guidance |
| 📦 | **Dependency Check** | Verify rclpy, colcon, ament and other key components |
| 🚀 | **Setup Guidance** | Step-by-step installation guidance for your platform |

---

## 📚 ROS2 Version Reference

| Version | Type | Support Period | Ubuntu | Status |
|:-:|:-:|:-:|:-:|:-:|
| **Humble Hawksbill** | LTS (5 years) | 2022 – 2027 | 22.04 | 🟢 Recommended |
| **Jazzy Jalisco** | LTS (3 years) | 2024 – 2027 | 24.04 | 🟢 Active |
| **Iron Irwini** | Regular | 2023 – 2024 | 22.04 | 🔴 EOL |
| **Rolling Ridley** | Rolling dev | Continuous | Latest | 🟡 Bleeding edge |

### 🎯 Which version should I choose?

| Scenario | Recommended |
|----------|:-----------:|
| 🌱 Beginner / Production / Need maximum stability | **Humble** |
| ⚡ Want newer features, still stable | **Jazzy** |
| 🔬 Developer / Testing latest features | **Rolling** |

---

## 🔎 What It Checks

| Check Item | Windows | WSL |
|-----------|:-------:|:---:|
| Environment variables (`ROS_DISTRO`, etc.) | ✅ | ✅ |
| Installation paths (`C:\dev\ros2_*`, `/opt/ros/`) | ✅ | ✅ |
| `ros2` command availability | ✅ | ✅ |
| Python `rclpy` module | ✅ | ✅ |
| `colcon` / `ament` build tools | ✅ | ✅ |
| Workspace setup scripts | ✅ | ✅ |

---

## 💡 Common Issues & Solutions

### ❌ `ros2: command not found`
**Cause**: Setup script not sourced / not in PATH
**Fix**:
- Windows: run `C:\dev\ros2_humble\setup.bat`
- WSL/Linux: `source /opt/ros/humble/setup.bash`

### ❌ `rclpy` import error
**Cause**: Python environment mismatch or ROS2 not properly installed
**Fix**: Reinstall ROS2 or verify Python version compatibility (Python 3.10+)

### ❌ ROS2 works in Windows but not in WSL
**Cause**: Windows and WSL environments are completely separate
**Fix**: Install ROS2 inside WSL separately — they don't share installations

---

## 🚀 Quick Start

### Prerequisites
- TRAE Workspace
- ROS2 installed (or about to install 😄)

### Installation
1. Clone or download this skill
2. Place it under `.trae/skills/ros2-env-manager/` in your workspace
3. Restart TRAE or reload skills

### Usage
Just ask TRAE:
```
"检查我的 ROS2 环境状态"
"ROS2 Humble 和 Jazzy 有什么区别？"
"WSL 里怎么安装 ROS2？"
"我的 rclpy 导入失败了怎么办？"
```

---

## 📁 File Structure

```
ros2-env-manager/
├── 📄 README.md      # This file — you're reading it!
└── 📄 SKILL.md       # Skill definition for TRAE platform
```

---

## 🌟 Why This Skill?

> ROS2 environment setup can be painful, especially on Windows.
> This skill saves you from hours of troubleshooting —
> **check, diagnose, fix — all in one conversation.**

---

## 📄 License

[MIT](LICENSE) © monicaffy108-alt

---
---

# 🤖 ROS2 环境管理器

> **一键诊断 & 管理你的 ROS2 开发环境**
>
> _一款用于 Windows 和 WSL 下 ROS2 环境诊断与管理的 TRAE 技能_

---

## ✨ 功能介绍

告别手动排查 ROS2 环境问题的烦恼！这个技能帮你快速诊断、对比和修复 ROS2 环境，新手老手都好用。

| | 功能 | 说明 |
|---|---|---|
| 🔍 | **环境检测** | 一键扫描 Windows 和 WSL 下的 ROS2 安装状态 |
| 📊 | **版本对比** | Humble、Jazzy、Rolling — 帮你选对版本 |
| 🛠️ | **故障排查** | 常见问题？直接给你解决方案和修复指引 |
| 📦 | **依赖检查** | 验证 rclpy、colcon、ament 等核心组件 |
| 🚀 | **安装指导** | 根据你的平台提供分步安装指南 |

---

## 📚 ROS2 版本参考

| 版本 | 类型 | 支持周期 | Ubuntu 版本 | 状态 |
|:-:|:-:|:-:|:-:|:-:|
| **Humble Hawksbill** | LTS（5年） | 2022 – 2027 | 22.04 | 🟢 推荐使用 |
| **Jazzy Jalisco** | LTS（3年） | 2024 – 2027 | 24.04 | 🟢 活跃维护 |
| **Iron Irwini** | 普通版 | 2023 – 2024 | 22.04 | 🔴 已停止维护 |
| **Rolling Ridley** | 滚动开发版 | 持续更新 | 最新版 | 🟡 前沿版本 |

### 🎯 我该选哪个版本？

| 使用场景 | 推荐版本 |
|----------|:-------:|
| 🌱 新手入门 / 生产环境 / 追求稳定 | **Humble** |
| ⚡ 想要新功能，又要稳定性 | **Jazzy** |
| 🔬 开发者 / 测试最新功能 | **Rolling** |

---

## 🔎 检测内容一览

| 检测项目 | Windows | WSL |
|-----------|:-------:|:---:|
| 环境变量（`ROS_DISTRO` 等） | ✅ | ✅ |
| 安装路径（`C:\dev\ros2_*`、`/opt/ros/`） | ✅ | ✅ |
| `ros2` 命令是否可用 | ✅ | ✅ |
| Python `rclpy` 模块 | ✅ | ✅ |
| `colcon` / `ament` 构建工具 | ✅ | ✅ |
| 工作空间启动脚本 | ✅ | ✅ |

---

## 💡 常见问题与解决方案

### ❌ `ros2: command not found`（找不到命令）
**原因**：没有执行 setup 脚本 / 环境变量没配置
**解决方法**：
- Windows：运行 `C:\dev\ros2_humble\setup.bat`
- WSL/Linux：执行 `source /opt/ros/humble/setup.bash`

### ❌ `rclpy` 导入失败
**原因**：Python 环境不匹配或 ROS2 安装不完整
**解决方法**：重新安装 ROS2，或检查 Python 版本兼容性（需 Python 3.10+）

### ❌ Windows 能用 ROS2，但 WSL 里用不了
**原因**：Windows 和 WSL 是完全独立的环境
**解决方法**：在 WSL 内部单独安装 ROS2，两边不共享安装

---

## 🚀 快速开始

### 前置条件
- TRAE 工作区
- 已安装 ROS2（或者正准备安装 😄）

### 安装方法
1. 克隆或下载本技能
2. 放入工作区的 `.trae/skills/ros2-env-manager/` 目录下
3. 重启 TRAE 或重新加载技能

### 使用方式
直接问 TRAE 就行：
```
"检查我的 ROS2 环境状态"
"ROS2 Humble 和 Jazzy 有什么区别？"
"WSL 里怎么安装 ROS2？"
"我的 rclpy 导入失败了怎么办？"
```

---

## 📁 文件结构

```
ros2-env-manager/
├── 📄 README.md      # 本文件 —— 你正在看的就是！
└── 📄 SKILL.md       # TRAE 平台技能定义文件
```

---

## 🌟 为什么做这个技能？

> ROS2 环境配置，尤其是在 Windows 上，经常让人头大。
> 这个技能帮你省去几小时的排查时间——
> **检测、诊断、修复，一次对话全搞定。**

---

## 📄 开源协议

[MIT](LICENSE) © monicaffy108-alt

---

<div align="center">

**如果对你有帮助，别忘了给个 ⭐ Star 哦！**

Made with 🤖 by monicaffy108-alt

</div>
