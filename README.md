# 美国站产品视频本地化

一个可复用的 Codex 技能，用于把美国站英文产品视频中的卖点、标签和字幕转换为德语、法语、西班牙语等语言，并按语言导出 MP4。

## 快速开始

1. 将本仓库的 [SKILL.md](SKILL.md) 放入本机 Codex 技能目录下的 `localize-us-product-video` 文件夹，形成 `~/.codex/skills/localize-us-product-video/SKILL.md`。如果设置了 `CODEX_HOME`，请使用它下面的 `skills` 目录。
2. 在 Codex 中提供原始 MP4 或可编辑的 Canva 工程链接，并说明目标语言。
3. 在对话中调用技能。例如：

   > 用 $localize-us-product-video，把这条美国站产品视频做成德语、法语、西班牙语三个 MP4。保留原音轨，沿用 035 的文字置顶样式。

## 按素材选择工具

| 素材或需求 | 处理方式 |
| --- | --- |
| 有可编辑的 Canva 工程 | 用 Canva 插件检查文字图层，替换文案并检查时间点、动画和排版。 |
| 给英文旁白加翻译字幕 | 用 [Canva 网页编辑器的 Captions](https://www.canva.com/help/generate-edit-captions-on-videos/) 生成、翻译和校对字幕。 |
| 英文已经嵌入 MP4 画面 | 用 FFmpeg、FFprobe 和 ASS（libass）或同类剪辑工具检查镜头、重新取景、按时间叠加译文并导出。 |
| 静态片尾图片有英文 | 可用 [Canva Magic Eraser](https://www.canva.com/help/magic-eraser/) 处理静态图，再将结果合成到视频。 |

仅使用本地 MP4 时，可以直接走本地剪辑流程。Canva 网页版的字幕功能处理旁白，画面上的烧录卖点仍需单独编辑。

## 035 样式与验收

- 产品镜头铺满画幅，德语卖点用顶部居中的白字和细深色描边，采用无黑边、无爱心、无文字底板的排版。
- 片尾房间名称分别对齐对应图片，保留原音轨和品牌标志。
- 按镜头检查原英文残字、重影、模糊带、裁切影响与时间点，并检查重音字符和长文案的可读性。
- 每种语言单独出片，例如 `035-DE.mp4`、`035-FR.mp4` 和 `035-ES.mp4`。如需核对上架条件，以目标站点的当前官方要求为准。

详细流程见 [SKILL.md](SKILL.md)。
