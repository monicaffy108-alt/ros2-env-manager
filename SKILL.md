---
name: "ros2-env-manager"
description: "Diagnoses and manages ROS2 environments on Windows and WSL. Invoke when user asks about ROS2 installation status, version comparisons, environment setup, or troubleshooting ROS2 issues."
---

# 🤖 ROS2 环境管理器

> 一键诊断 & 管理你的 ROS2 开发环境

## 触发条件

当用户询问以下话题时激活本技能：

- 🔍 ROS2 是否已安装 / 检查 ROS2 环境状态
- 📊 ROS2 版本区别（Humble / Jazzy / Rolling 等）
- 🛠️ ROS2 安装建议与路径指导
- ⚙️ ROS2 环境变量问题排查
- 🐧 WSL 中的 ROS2 状态检查
- ❌ `ros2` / `rclpy` / `colcon` 等命令报错

---

## 核心能力

### 1️⃣ 环境检查

全面扫描 ROS2 环境状态，检查以下位置：

| 检查项 | Windows | WSL |
|--------|:-------:|:---:|
| 环境变量（`ROS_DISTRO`、`AMENT_PREFIX_PATH`、`ROS_VERSION`） | ✅ | ✅ |
| 常见安装路径（`C:\dev\ros2_*`、`/opt/ros/`） | ✅ | ✅ |
| `ros2` 命令是否可用 | ✅ | ✅ |
| Python `rclpy` 模块 | ✅ | ✅ |
| `colcon` / `ament` 构建工具 | ✅ | ✅ |
| 工作空间 setup 脚本 | ✅ | ✅ |

---

### 2️⃣ 版本知识

ROS2 版本按字母表顺序命名（**形容词 + 龟/爬行动物**）：

| 版本 | 类型 | 支持周期 | 对应 Ubuntu | 状态 |
|------|------|---------|------------|------|
| **Humble Hawksbill** | LTS（5年） | 2022 – 2027 | 22.04 | 🟢 推荐 |
| **Jazzy Jalisco** | LTS（3年） | 2024 – 2027 | 24.04 | 🟢 活跃 |
| **Iron Irwini** | 普通版 | 2023 – 2024 | 22.04 | 🔴 EOL |
| **Rolling Ridley** | 滚动开发版 | 持续更新 | 最新版 | 🟡 前沿 |

#### 🎯 版本选择建议

| 使用场景 | 推荐版本 |
|----------|---------|
| 🌱 初学者 / 生产环境 / 追求稳定 | **Humble**（教程最多、生态最完善） |
| ⚡ 想要新功能，又要稳定性 | **Jazzy** |
| 🔬 开发者 / 测试最新功能 | **Rolling** |

---

### 3️⃣ 安装路径参考

| 平台 | 默认安装路径 | 激活方式 |
|------|------------|---------|
| **Windows** | `C:\dev\ros2_humble\` 或 `C:\opt\ros\humble\x64\` | 运行 `setup.bat` |
| **WSL / Ubuntu** | `/opt/ros/humble/` | `source /opt/ros/humble/setup.bash` |

> 💡 **注意**：Windows 和 WSL 的 ROS2 是完全独立的，需要分别安装，互不共享。

---

### 4️⃣ 常见问题排查

#### ❌ `ros2: command not found`（找不到命令）
- **原因**：未添加到 PATH 或未运行 setup 脚本
- **解决**：
  - Windows：执行 `C:\dev\ros2_humble\setup.bat`
  - WSL：执行 `source /opt/ros/humble/setup.bash`

#### ❌ `rclpy` 找不到 / 导入失败
- **原因**：Python 环境不匹配或 ROS2 未正确安装
- **解决**：重新安装 ROS2，或检查 Python 版本兼容性（需 Python 3.10+）

#### ❌ WSL 中没有 ROS2
- **原因**：WSL 和 Windows 环境相互独立
- **解决**：在 WSL 内单独安装 ROS2

---

### 5️⃣ 诊断输出格式

检查完成后，按以下结构输出结果：

```
🤖 ROS2 环境诊断报告
━━━━━━━━━━━━━━━━━━━━

📋 基本信息
  • 检测平台：Windows / WSL / 双环境
  • 检测时间：xxxx-xx-xx

✅ 已检测到的组件
  • ROS2 版本：Humble Hawksbill
  • 安装路径：C:\dev\ros2_humble\
  • rclpy：正常
  • colcon：正常

⚠️ 发现的问题
  • 问题1：描述 + 建议

💡 下一步建议
  • 建议1
  • 建议2
```

---

## 技能元信息

- **技能名称**：ros2-env-manager
- **适用平台**：Windows / WSL / Linux
- **ROS2 版本**：Humble / Jazzy / Rolling
- **作者**：monicaffy108-alt
- **协议**：MIT
