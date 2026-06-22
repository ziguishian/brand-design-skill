<h1 align="center">Brand Design Skill</h1>

<p align="center">
  一个面向 Codex 的品牌设计 Skill，用于把粗略品牌想法转化为专业的 image-first 品牌识别系统、VI 规范与可编辑 HTML 品牌手册。
</p>

<p align="center">
  <a href="README.md">English</a>
  ·
  <a href="SKILL.md">Skill 提示词</a>
  ·
  <a href="references/design-output-standards.md">输出标准</a>
  ·
  <a href="examples/haitao/brand-manual.html">案例手册</a>
</p>

<p align="center">
  <img src="assets/banner.png" alt="Brand Design Skill banner" />
</p>

## 它能做什么

Brand Design Skill 会让 Codex 以资深品牌设计总监的方式工作，而不是只生成一个装饰性 Logo。它会引导模型完成品牌策略、概念解析、苏格拉底式澄清、设计方向、AI Logo 图像探索、最终图像 Logo 资产、VI 规则、应用图像，以及高质量 HTML 品牌手册。

## 亮点

- 将模糊创意 brief 转化为结构化品牌识别系统。
- 在生成视觉前先提出关键设计问题。
- 生成结构明显不同的 Logo 图像方向。
- 使用 image-first / image-final 流程，不再依赖容易出错的 SVG 重构。
- 生成多个行业相关的应用场景图。
- 输出高质量 HTML 手册，包含色值复制、真实字体样张、图像 atlas 复用、响应式布局和克制微动效。
- 保护图像比例，避免应用图被拉伸或压扁。

## 主案例

### 海涛水杯品牌 VI 手册

当前主案例是 **海涛 HAITAO** 水杯品牌，从对话 brief、Logo 图像探索、最终 Logo 图像资产、多张应用图、类雪碧图 atlas 到可编辑 HTML VI 手册完整跑通。

<p align="center">
  <img src="examples/haitao/applications/haitao-application-atlas.png" alt="由 skill 生成的海涛应用场景 atlas" />
</p>

- HTML 品牌手册：[`examples/haitao/brand-manual.html`](examples/haitao/brand-manual.html)
- 最终 Logo 图像资产：[`examples/haitao/final-logo/haitao-final-logo-assets-v1.png`](examples/haitao/final-logo/haitao-final-logo-assets-v1.png)
- 应用场景 atlas：[`examples/haitao/applications/haitao-application-atlas.png`](examples/haitao/applications/haitao-application-atlas.png)
- 完整测试记录：[`examples/haitao/`](examples/haitao/)

## 更多示例

- 小鸭咸鸭蛋 Logo 图像探索：[`examples/xiaoya/generated/logo-contact-sheet-v1.png`](examples/xiaoya/generated/logo-contact-sheet-v1.png)
- 西北食品品牌 image-first 流程测试：[`examples/xibei/`](examples/xibei/)
- 科技吸尘器品牌对话关卡测试：[`examples/vacuum-tech2/`](examples/vacuum-tech2/)

## 工作流

```text
粗略 brief
  -> 苏格拉底式澄清
  -> 设计方向选项
  -> Logo 图像生成
  -> 用户选择 / 调整
  -> 最终 Logo 图像资产
  -> VI 应用图像
  -> 交互式 HTML 品牌手册
```

这个 skill 是严格门控的：不应从不完整 brief 直接生成图像，不应跳过用户选择，不应创建 SVG Logo，也不应在最终 Logo 图像资产确认前渲染完整手册。

## 项目结构

```text
brand-design-skill/
├─ SKILL.md
├─ agents/
│  └─ openai.yaml
├─ assets/
│  ├─ banner.png
│  ├─ logo.png
│  ├─ banner.svg
│  ├─ banner-generation-prompt.md
│  └─ logo.svg
├─ examples/
│  ├─ haitao/
│  ├─ xiaoya/
│  ├─ xibei/
│  └─ vacuum-tech2/
└─ references/
   ├─ conversational-workflow.md
   ├─ design-output-standards.md
   └─ industry-and-manual-scope.md
```

## 流程参考

- [references/conversational-workflow.md](references/conversational-workflow.md)：对话关卡和阶段行为。
- [references/industry-and-manual-scope.md](references/industry-and-manual-scope.md)：行业适配和手册深度。
- [references/design-output-standards.md](references/design-output-standards.md)：QA、图像资产、HTML 和手册标准。

## 安装方式

将本文件夹复制或克隆到你的 Codex skills 目录：

```bash
~/.codex/skills/brand-design-skill
```

然后在 Codex 中这样调用：

```text
Use $brand-design-skill to create a professional brand identity system and HTML brand manual.
```

## 示例提示词

```text
Use $brand-design-skill to design a VI system for a premium drinkware brand.
```

```text
Use $brand-design-skill to create a logo, VI system, application images, and HTML brand manual for a boutique coffee brand.
```

```text
Use $brand-design-skill to turn this rough idea into a premium identity system: a cultural technology studio connecting museums and interactive media.
```

## Star History

开源发布后，请将下面链接中的 `YOUR_GITHUB_USERNAME` 替换为你的 GitHub 账号或组织名。

<a href="https://star-history.com/#YOUR_GITHUB_USERNAME/brand-design-skill&Date">
  <img src="https://api.star-history.com/svg?repos=YOUR_GITHUB_USERNAME/brand-design-skill&type=Date" alt="Star History Chart" />
</a>

## 参与贡献

欢迎贡献。适合改进的方向包括：更清晰的对话门控、更丰富的行业 playbook、更严格的图像资产规则、更高级的 HTML 手册模式，以及更真实的示例提示词。

## 许可证

开源发布前请补充你偏好的许可证，例如 MIT、Apache-2.0 或 CC BY 4.0。
