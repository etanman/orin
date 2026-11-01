<img width="1475" height="950" alt="image" src="https://github.com/user-attachments/assets/85b22459-1d62-41b9-9ccf-23bd8a91a664" />
<img width="1475" height="950" alt="image" src="https://github.com/user-attachments/assets/9361c572-7354-4479-b9b0-fc088a24d464" />

# Orin

一个简洁、沉浸式的跨平台本地音乐播放器。

Orin 追求"开箱即听"的纯粹体验：没有联网账号、没有广告，专注于本地音乐的解码与播放。内置多套沉浸式播放界面（唱机 / 唱片 / CD / 磁带 / 时钟），配合频谱与环绕光斑，让听歌这件事更有仪式感。


å
## ✨ 特性

- **多格式解码**：支持 FLAC / APE / WAV / MP3 / ALAC 等多种音频格式，基于裁剪过的 FFmpeg 解码引擎，仅保留音频能力，体积更小。
- **沉浸式播放界面**：唱机、唱片、CD、磁带、时钟等动态封面，随播放律动的频谱样式（琉璃光柱、流星坠雨、涟漪波痕、繁星律动、霓虹音阶、炫彩灯条）。
- **多播放列表**）：「默认列表 / 我喜爱的」等，支持新建、重命名、清空、复制、删除。
- **完整曲库管理**：专辑分组、搜索过滤、拖拽排序、CUE / M3U / 压缩包（ZIP / RAR / 7Z）直接导入。
- **专业音频控制**：图形 EQ（多档预设）、低音 / 中音 / 高音、速度 / 变调调节、输出设备切换、系统音量控制。
- **歌词**：在线匹配歌词，支持复制与下载到本地。
- **CD 播放**：支持音频 CD 的读取与播放。
- **多语言**：简体中文 / 繁體中文 / English 界面切换。
- **主题与布局**：深色 / 浅色主题，左右栏比例与窗口大小可调。

## 🖥️ 平台支持

| 平台 | 说明 |
| ---- | ---- |
| Windows | 自带无边框自绘标题栏 |
| macOS | 原生标题栏、原生菜单栏托盘图标、标准 Dock 图标 |
| Linux | 支持 GTK3，提供 `.deb` 打包 |

## 🛠️ 技术栈

- **框架**：[Wails](https://wails.io/) v3（Go + Web 前端）
- **后端**：Go，自研音频引擎（基于 [oto](https://github.com/ebitengine/oto) 直送声卡）
- **解码**：裁剪版 [FFmpeg](https://ffmpeg.org/)（仅音频解复用 / 解码 / 滤镜），构建脚本见 `scripts/build-ffmpeg-*.sh`
- **前端**：原生 HTML / CSS / JavaScript

## 🚀 构建

构建脚本位于项目根目录与 `scripts/` 下：

```bash
# Windows（在 PowerShell 中）
.\build.ps1               # 生成 orin.exe

# macOS
bash build-macos.sh

# Linux（打包 .deb）
bash scripts/build-all.sh
```

> FFmpeg 共享库需先按各平台脚本编译定制版本（`scripts/build-ffmpeg-linux.sh` / `-macos.sh` / `-windows.sh`），构建脚本已包含对产物路径的处理。

## 📝 使用提示

- 将歌曲或文件夹拖入窗口即可开始播放。
- 支持 CUE / M3U / ZIP / RAR / 7Z 直接导入。
- 关于对话框右下角提供了「问题反馈」（GitHub Issues）与「支持作者」入口。

## 🤝 反馈与支持

- 遇到问题或提出建议，欢迎到 [Issues](https://github.com/etanman/orin/issues) 反馈。
- 如果你喜欢 Orin，欢迎通过 [爱发电](https://afdian.com/a/orin-player) 支持作者。
