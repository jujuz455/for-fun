# 🌸 Sakura AR: Hand Gesture Summoning System

[中文说明](#中文说明) | [English Description](#english-description)

![Project Banner](https://via.placeholder.com/1000x300?text=Sakura+AR+System+v30.0)
*(建议上传一张运行截图替换上方链接 / You can replace this link with a screenshot)*

## 📖 English Description

**Sakura AR** is a browser-based Augmented Reality (WebAR) experiment that allows users to summon 3D characters and magic circles using specific hand gestures. Built with **Three.js** and **Google MediaPipe**, it runs entirely in the browser without requiring any app installation.

### ✨ Key Features
* **Real-time Hand Tracking**: High-precision hand skeleton tracking via MediaPipe.
* **Multi-Character Summoning**: Summon Hatsune Miku, Maomao, and Klee with different gestures.
* **Procedural Magic Circle**: High-definition magic circle with particle effects and dynamic lighting.
* **Dynamic Interaction**: Control position, rotation, and scale of models with hand movements.
* **Audio Feedback**: Procedural sound effects (Synth) generated via Web Audio API.
* **Auto-Normalization**: Automatically scales imported 3D models to standard sizes.

### 🎮 Controls & Gestures

| Gesture | Action | Description |
| :--- | :--- | :--- |
| **✌️ Victory (Peace Sign)** | **Summon Miku** | Summons Hatsune Miku. |
| **✋ Single Open Palm** | **Summon Maomao** | Summons Maomao (The Apothecary Diaries). |
| **👐 Vertical Hands** | **Summon Klee** | Hold hands vertically (one above another). Distance controls size. |
| **✊ Closed Fist** | **Dismiss** | Hides all models and magic circles. |
| **↔️ Two Index Fingers** | **Resize Circle** | Move fingers apart to resize the magic circle. |
| **🙌 Two Open Palms** | **Lock/Unlock** | Toggle size locking (10s cooldown). Prevents accidental resizing. |
| **☝️ Single Pointing** | **Control Circle** | Move the magic circle with particles. |

### 🚀 How to Run

1.  **Clone or Download** this repository.
2.  **Prepare Assets**: Ensure the following files are in the root directory (names must match exactly):
    * `index.html` (The main code)
    * `sakura_circle.png` (Transparent magic circle image)
    * `miku_hatsune__wasabi.glb`
    * `maomao_the_apothecary_diaries.glb`
    * `klee_genshin_impact.glb`
3.  **Start Local Server**:
    * Due to browser CORS security policies, you **cannot** run this by double-clicking the HTML file.
    * **Recommended**: Use VS Code and install the **"Live Server"** extension. Right-click `index.html` and select "Open with Live Server".
    * **Alternative**: Run `python -m http.server` in the terminal.
4.  **Allow Permissions**: Allow camera access when prompted.

---

## 📖 中文说明

**Sakura AR** 是一个基于浏览器的增强现实 (WebAR) 系统。它利用 **Three.js** 进行 3D 渲染，并使用 **Google MediaPipe** 进行高性能手势识别。用户可以通过特定的手势召唤二次元角色、控制魔法阵大小并触发炫酷的粒子特效。

### ✨ 核心功能
* **实时手势追踪**：基于 MediaPipe 的高精度手部骨骼识别。
* **多角色召唤系统**：通过不同手势召唤初音未来、猫猫（药屋少女）和可莉（原神）。
* **高清魔法阵**：加载原版百变小樱魔法阵，通过代码实现辉光与旋转动画。
* **动态粒子系统**：基于距离场的粒子喷射效果，随动作快慢变化。
* **程序化音效**：无需音频文件，使用 Web Audio API 实时合成“Biu~”的科技感音效。
* **智能缩放**：自动计算 3D 模型边界框，将不同比例的模型统一到标准高度。

### 🎮 手势操作指南

| 手势动作 | 功能 | 详细说明 |
| :--- | :--- | :--- |
| **✌️ 比耶 (剪刀手)** | **召唤 Miku** | 手心显示初音未来模型，自带旋转动画。 |
| **✋ 单手托举 (张开手掌)** | **召唤猫猫** | 手心显示猫猫 (药屋少女的呢喃)。 |
| **👐 双手上下平行** | **召唤可莉 (Klee)** | 双手一上一下虚抱。拉开双手距离可让可莉变大。 |
| **✊ 握拳** | **消失/重置** | 隐藏所有模型和魔法阵，重置状态。 |
| **↔️ 双手食指** | **调整大小** | 拉开两根食指的距离，调整魔法阵大小。 |
| **🙌 双手十指张开** | **锁定/解锁** | 锁定当前大小（防止误触）。再次张开可解锁。 |
| **☝️ 单手操控** | **移动法阵** | 在未触发召唤时，单手控制魔法阵移动和甩出粒子。 |

### 📂 文件结构说明

运行本项目前，请确保目录中包含以下文件（文件名必须完全一致）：

```text
/Project_Folder
│
├── index.html                        # 核心代码 (v30.0)
├── sakura_circle.png                 # 透明背景的魔法阵图片
├── miku_hatsune__wasabi.glb          # 3D 模型文件 1
├── maomao_the_apothecary_diaries.glb # 3D 模型文件 2
└── klee_genshin_impact.glb           # 3D 模型文件 3
