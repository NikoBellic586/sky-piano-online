# Sky Piano Online (Sky 乐器 - 沉浸式增强版)

[简体中文](#简体中文) | [English](#english)

---

<a name="简体中文"></a>

## 简体中文

一款基于原生 Web 技术构建的沉浸式虚拟钢琴演奏工具。项目复刻了《光遇》（Sky: Children of the Light）中的 15 键乐器排布，并在此基础上进行了功能增强，支持完整的半音演奏、自由音高控制以及个性化外观定制。

👉 **[在线体验 / Live Demo](https://nikobellic586.github.io/sky-piano-online/)**

### ✨ 核心功能与技术实现

- **纯 Web 动态合成音频**：无需加载大体积的音频样本文件。项目使用 **Web Audio API** 动态创建 `AudioContext`，通过三角形波（`triangle`）振荡器配合指数衰减（`exponentialRampToValueAtTime`）实现干净柔和的乐器音色。
- **完整的半音支持（变调功能）**：
  - 支持 **升半音 (♯)** 与 **降半音 (♭)**，让网页乐器能演奏更复杂的半音阶曲目。
  - 拥有两种变调模式：
    - **保持模式 (Hold)**：按下变调键时生效，松开立即恢复原调。
    - **开关模式 (Toggle)**：点击后持续生效，再次点击恢复。
- **宽广的音域控制**：提供八度音高偏移调节（`-3` 至 `+3` 八度），支持通过键盘或面板一键切换。
- **沉浸式视觉与动效**：
  - 基于 **HTML5 Canvas** 渲染的动态星空背景。
  - 优雅的毛玻璃（Glassmorphism）UI 设计。
  - 侧边栏支持流畅的滑入动画与移动端自定义极细滚动条。
- **高度个性化**：支持用户上传本地图片作为演奏背景（内置防重复上传机制及大图体积提示限制），并支持一键恢复至初始星空渐变。
- **全平台自适应**：利用 CSS Media Queries 和等比缩放（Scale）机制，在不同分辨率的屏幕（PC、手机、平板）上均能提供合理的按键尺寸。

### ⌨️ 按键操作指南

#### 1. 乐器音符映射 (15 键排列)
乐器按键布局分为三行，对应标准键盘按键如下：

| 第一行 (高音区) | `Y` | `U` | `I` | `O` | `P` |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **第二行 (中音区)** | `H` | `J` | `K` | `L` | `;` |
| **第三行 (低音区)** | `N` | `M` | `,` | `.` | `/` |

#### 2. 功能控制键

| 操作 | 对应键盘按键 | 说明 |
| :--- | :---: | :--- |
| **升八度 (+1 Octave)** | `Alt` | 提高演奏整体音高 |
| **降八度 (-1 Octave)** | `Space` (空格键) | 降低演奏整体音高 |
| **降半音 (♭ / Flat)** | `G` | 降低当前演奏音半步（降半音） |
| **升半音 (♯ / Sharp)** | `'` (单引号) | 提高当前演奏音半步（升半音） |

---

<a name="english"></a>

## English

An immersive web-based virtual piano tool inspired by *Sky: Children of the Light*. This project replicates the game's classic 15-key layout while introducing enhanced features such as full semitone support, flexible pitch shifting, and personalized visual customization.

👉 **[Live Demo](https://nikobellic586.github.io/sky-piano-online/)**

### ✨ Key Features & Technical Details

- **Dynamic Audio Synthesis**: Free from heavy audio sample downloads. The app leverages the native **Web Audio API** (`AudioContext`) to generate soft, crisp instrumental tones dynamically via `triangle` oscillators and exponential decay envelopes (`exponentialRampToValueAtTime`).
- **Comprehensive Semitone Support**:
  - Adds **Sharp (♯)** and **Flat (♭)** modifiers, allowing you to play complex melodies beyond the basic diatonic scale.
  - Offers two modulation behaviors:
    - **Hold Mode**: Modifier triggers on key down and releases immediately on key up.
    - **Toggle Mode**: Clicking the modifier locks the state until it is pressed again.
- **Wide Octave Control**: Shift the octave range freely via on-screen buttons or keyboard shortcuts.
- **Immersive Visuals & Aesthetics**:
  - A real-time floating starfield background rendered on an **HTML5 Canvas**.
  - Elegant Glassmorphism interface.
  - A slide-out sidebar that auto-collapses when clicking outside, equipped with tailored thin scrollbars.
- **Visual Personalization**: Upload local images using the `FileReader` API to customize your background wallpaper (includes 10MB size limit check and input resetting logic). Reset back to the default starry gradient at any time.
- **Responsive Layout**: Adapts smoothly to various viewports (mobiles, tablets, PCs) using CSS media queries combined with precise scaling transforms.

### ⌨️ Controls & Key Mappings

#### 1. Instrument Note Mapping (15 Keys Grid)
The instrument keyboard layout consists of three rows mapped directly to standard keyboard inputs:

| Row 1 (High) | `Y` | `U` | `I` | `O` | `P` |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Row 2 (Mid)** | `H` | `J` | `K` | `L` | `;` |
| **Row 3 (Low)** | `N` | `M` | `,` | `.` | `/` |

#### 2. Function Shortcuts

| Action | Keyboard Shortcut | Description |
| :--- | :---: | :--- |
| **Octave Up (+1)** | `Alt` | Increases the overall pitch by an octave. |
| **Octave Down (-1)** | `Space` | Decreases the overall pitch by an octave. |
| **Flat Modifier (♭)** | `G` | Lowers the note by a semitone. |
| **Sharp Modifier (♯)** | `'` (Single Quote) | Raises the note by a semitone. |
