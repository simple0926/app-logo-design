# App Logo Design / App Logo 设计

[中文](#中文) · [English](#english)

## 中文

一个从品牌主张出发、以 Android 和 iOS 图标资源包为完整交付终点的设计 skill。它帮助用户先决定陌生人应该如何理解产品、产生什么感受，再选择视觉风格并生成方案。

### 工作流程

1. **确认产品判断**：第一理解、第一感受、品牌主张与误读边界。复用已经确认的信息。
2. **形成统一视觉命题**：明确表达的产品结果；未指定具体画面时，不提前锁定所有方案的母题。
3. **看图选择 1–3 种风格**：拟物材质、扁平极简、文字字标、渐变光感、立体空间、插画叙事。六类是沟通入口，不是 Apple 官方分类。
4. **分别构思和生图**：不同风格围绕同一品牌主张设计内容。已授权生成且未另定数量时，每种先出一张；明确的数量与保留要求优先。
5. **检查与迭代**：检查实际图像、目标尺寸、可能的品类误读。只有用户明确要求时，才将多风格探索限定为同一内容换画法。
6. **确认最终设计**：用户选定最终稿，再开始生产适配；不替所有候选提前打包。
7. **交付双平台资源**：按项目与当前平台规范，生成 Android、iOS 各一套文件、接入说明和验证记录。

### 六类风格参考

| S1 · 拟物材质 | S2 · 扁平极简 | S3 · 文字字标 |
|---|---|---|
| ![Crouton：拟物材质](assets/style-references/s1-crouton.jpg) | ![Blackbox：扁平极简](assets/style-references/s2-blackbox.jpg) | ![NYT Games：文字字标](assets/style-references/s3-nyt-games.jpg) |
| Crouton | Blackbox | NYT Games |
| **S4 · 渐变光感** | **S5 · 立体空间** | **S6 · 插画叙事** |
| ![Procreate Dreams：渐变光感](assets/style-references/s4-procreate-dreams.jpg) | ![Rooms：立体空间](assets/style-references/s5-rooms.jpg) | ![Bears Gratitude：插画叙事](assets/style-references/s6-bears-gratitude.jpg) |
| Procreate Dreams | Rooms | Bears Gratitude |

| 编号 | 方向 | 主要表达手段 |
|---|---|---|
| S1 | 拟物材质 | 熟悉实物、材质与光影 |
| S2 | 扁平极简 | 轮廓、色块与负空间 |
| S3 | 文字字标 | 名称、汉字与定制字形 |
| S4 | 渐变光感 | 连续色阶与光感 |
| S5 | 立体空间 | 体块、透视与构造 |
| S6 | 插画叙事 | 角色、动作与生活场景 |

参考样本来自 Apple Design Awards 获奖产品的 App 图标观察。**奖项表彰产品设计体验，并非图标单独获奖**；样本版本与来源见[参考目录](references/style-catalog.md)。不复制参考品牌的身份。

### 使用方式

将本目录作为 `app-logo-design` 放入支持 `SKILL.md` 的宿主技能目录。Codex 的常用位置是 `~/.codex/skills/app-logo-design/`；已有安装时先比较或备份，不直接覆盖个人修改。重新打开会话或按宿主方式刷新技能发现。

示例：

```text
使用 $app-logo-design，为我的生活预算 App 设计图标。
品牌主张：有规划、有实践，把握自己的花费和生活。
先展示风格参考，让我选择 1–3 种。
```

```text
品牌主张保持不变，选择拟物材质和插画叙事。
每种先设计一张，分别构思内容，不使用旧图作为基线。
```

```text
这张确定为最终稿。请按项目生成 Android 和 iOS 两套图标资源包，
附开发接入说明，并区分已验证与尚未验证的项目。
```

### 运行条件与交付范围

- 这是供设计代理执行的工作流，不是独立生图程序或一键发布脚本。宿主需要文件读写能力；生成实际图片需要可用的生图工具，研究当前平台要求需要网络访问。
- 优先使用宿主原生 imagegen。不会为了使用本 skill 默认要求 API key，也不会静默切换到第三方付费后端。其他宿主的工具可用性需单独确认。
- 工程构建与显示验证需要相应项目、SDK、Xcode、模拟器或设备；缺少环境时明确标记未验证，不保证一张生成图即可上架。
- 完整交付包含独立的 Android、iOS 压缩包与可浏览目录。Android 包含适用的自适应图层、XML、兼容资源和商店资源；iOS 按工具链交付资产目录或真实 Icon Composer 资产。具体内容见[平台交付协议](references/platform-delivery.md)。
- 图片、资源交付、代码接入、构建通过和产品发布是不同状态。准备文件不代表自动上传商店或发布产品。
- 用户只要分析、提示词、概念或单平台交付时，遵循该范围。普通 UI 图标、页面设计、完整 VI 和商标注册不在默认范围。

### 文件导航

- [SKILL.md](SKILL.md)：执行入口。
- [风格参考](references/style-catalog.md)：真实案例、来源与选型方法。
- [提示词与迭代](references/prompt-contract.md)：统一主张与内容探索规则。
- [平台交付](references/platform-delivery.md)：Android / iOS 打包与验收。
- [案例与行为检查](references/case-and-checks.md)：实际纠偏案例及检查场景。
- [参考图集](assets/style-gallery.html)：内置六类参考小图与场景补充图，可离线查看；来源和版本信息见参考目录。
- [Release 说明](RELEASE_NOTES.md) · [第三方与许可说明](THIRD_PARTY_NOTICES.md)。

### 当前状态

`v0.1.0` 为首次版本。本 skill 源于“花在哪”的实际迭代，但没有宣称任何候选图已获最终确认、经过真实受众盲测或已上线。行为检查是验收场景，不能等同于自动化测试全部执行通过。

本次检查覆盖技能格式、本地引用与发布包结构；不代表已经运行完整的双平台生成、编译和上架流程。尚未选定仓库级许可证，当前没有 `LICENSE`；第三方品牌图标不属于本项目原创素材。

## English

A design skill that starts with a confirmed brand promise and ends, for a complete assignment, with separate Android and iOS app-icon resource packages. It helps establish what an unfamiliar person should understand and feel before choosing a visual style and generating concepts.

### Workflow

1. **Confirm the product judgment:** initial understanding, primary feeling, brand promise, and likely misinterpretations. Reuse decisions already confirmed.
2. **Define a shared visual proposition:** clarify the intended product outcome without prematurely imposing the same motif on every concept.
3. **Choose 1–3 styles using visual references:** tactile skeuomorphism, flat minimalism, wordmark/lettermark, gradients and light, dimensional space, or narrative illustration. These are practical discussion categories, not an official Apple taxonomy.
4. **Develop and generate each direction:** keep the brand promise consistent while designing content appropriate to each style. Once generation is authorized, default to one image per selected style unless the user specifies otherwise.
5. **Inspect and iterate:** review actual images, intended display sizes, and category confusion. Hold content constant across styles only when the user asks for that comparison or explicitly preserves content.
6. **Confirm the final design:** production packaging starts after explicit selection, not for every exploratory concept.
7. **Deliver platform resources:** prepare separate Android and iOS packages, integration instructions, and validation records for the actual project and current platform requirements.

### Style directions

| S1 · Tactile skeuomorphism | S2 · Flat minimalism | S3 · Wordmark / lettermark |
|---|---|---|
| ![Crouton: tactile materials](assets/style-references/s1-crouton.jpg) | ![Blackbox: reduced shapes](assets/style-references/s2-blackbox.jpg) | ![NYT Games: letterform identity](assets/style-references/s3-nyt-games.jpg) |
| Crouton | Blackbox | NYT Games |
| **S4 · Gradients and light** | **S5 · Dimensional space** | **S6 · Narrative illustration** |
| ![Procreate Dreams: gradients](assets/style-references/s4-procreate-dreams.jpg) | ![Rooms: dimensional space](assets/style-references/s5-rooms.jpg) | ![Bears Gratitude: narrative illustration](assets/style-references/s6-bears-gratitude.jpg) |
| Procreate Dreams | Rooms | Bears Gratitude |

| ID | Direction | Main visual language |
|---|---|---|
| S1 | Tactile skeuomorphism | Familiar objects, materials, and lighting |
| S2 | Flat minimalism | Silhouettes, color fields, and negative space |
| S3 | Wordmark / lettermark | Names, characters, and custom letterforms |
| S4 | Gradients and light | Color transitions and luminous shapes |
| S5 | Dimensional space | Volumes, perspective, and construction |
| S6 | Narrative illustration | Characters, actions, and everyday scenes |

References include app-icon observations from Apple Design Awards recipients. **The awards recognize product design experiences, not individual icon awards.** See the [catalog](references/style-catalog.md) for versions and sources; do not copy another brand's identity.

### Installation and use

Place this directory at `app-logo-design` inside a host's supported skill directory. A typical Codex location is `~/.codex/skills/app-logo-design/`. Compare or back up an existing installation before replacing it, then reopen the conversation or refresh skill discovery as supported by the host.

```text
Use $app-logo-design for a personal spending and life-planning app.
Brand promise: Plan, act, and take ownership of your spending and life.
Show visual references so I can choose 1–3 styles.
```

```text
Keep the brand promise. Explore tactile skeuomorphism and narrative illustration,
one concept each. Develop content independently; do not reuse an old image.
```

```text
This is the final design. Prepare separate Android and iOS icon packages
for the project, with integration steps and an honest validation record.
```

### Requirements and deliverables

- This is an agent workflow, not a standalone image generator or one-click publishing tool. The host needs file access; actual images require an available image-generation tool, and current platform research requires network access.
- Prefer the host's native imagegen. This skill does not require an API key by default or silently switch to a paid third-party backend. Tool availability in another host must be checked.
- Build and display validation require the relevant project, SDKs, Xcode, and a simulator or device. Missing checks must be disclosed; a generated image alone is not a release-ready app icon.
- A full delivery includes separate Android and iOS archives plus browsable directories. Android resources include applicable adaptive layers, XML, compatibility assets, and store artwork. iOS delivery uses the project's asset-catalog or genuine Icon Composer workflow. See [platform delivery](references/platform-delivery.md).
- Asset delivery, code integration, successful builds, and product publication are separate states. Preparing files does not authorize automatic store uploads or publishing.
- Respect narrower requests for analysis, prompts, concepts, or a single platform. General UI icons, page design, a full visual-identity system, and trademark registration are outside the default scope.

### Files and release status

Start with [SKILL.md](SKILL.md). Supporting references cover [styles](references/style-catalog.md), [prompts](references/prompt-contract.md), [platform packages](references/platform-delivery.md), and [case-based checks](references/case-and-checks.md). The [gallery](assets/style-gallery.html) includes local thumbnails for the six categories and a supplementary scene reference, so the visual gallery can be viewed offline. See the catalog for sources and observed versions.

`v0.1.0` is the initial version. The skill developed through iterations on “花在哪”, but no candidate is presented as a confirmed final logo, a tested audience success, or a shipped product. The behavioral checks are acceptance scenarios, not a claim that every automated test has run.

Checks for this preparation cover skill structure, local references, and package integrity. They do not establish an end-to-end Android/iOS build or store submission. No repository-wide license has been selected; no `LICENSE` is currently provided. Third-party app icons are not original project artwork.

See [release notes](RELEASE_NOTES.md) and [third-party notices](THIRD_PARTY_NOTICES.md).
