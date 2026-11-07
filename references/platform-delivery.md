# 定稿后的双平台图标资源交付

用户确认最终设计后读取。完整设计任务默认交付 Android、iOS 各一套，不能以一张图片结束；用户限定单平台、只要分析或概念时遵循其范围。这里的发布交付指准备开发和上架所需资源，不包含未经授权的上传或发布。

## 1. 确定接入方式，检查主稿

优先读取实际项目的图标目录、资源名、AndroidManifest、SDK 配置、Xcode 工程和资产目录；Flutter、React Native 等项目还要检查既有生成配置，避免下次构建又覆盖新图标。已有信息不重复问。没有工程时按原生约定生成独立资源包并说明接入假设，不声称已更新用户代码；仅在缺失信息会改变资源方案时问一个关键问题。

记录获选稿、版本、平台兼容范围和本次规范查询日期。先检查原始分辨率、色彩、背景与分层可用性，再进行导出。生成图不自动成为可编辑源文件；不能用放大小图冒充高清主稿，或把 PNG 嵌进 SVG 壳子称为矢量。需要的前景或背景图层缺失时，需要抠图、补背景或重绘，并复核没有改变定稿识别特征。重绘改变关键设计时回到用户确认。

发布主稿与效果预览分开：不要把设备截图、系统圆角或图标外部投影烘焙进主稿。是否保留图内光影及透明度按资产角色处理，不把所有文件统一抠透明。场景插画支持栅格素材，不强制矢量化或机械删掉故事。

## 2. Android 套装

依据项目实际 SDK、资源名和发布渠道制作：

- **应用资源**：保留可接入的 `res/` 相对目录。自适应彩色图标包含前景、背景及引用它们的 `<adaptive-icon>` XML，放入适用版本的 `mipmap-anydpi-*`；图层可按项目选用位图或 VectorDrawable。为本套交付制作可辨认的主题单色层，正确设置 `<monochrome>` 与版本兼容。它不是把全彩场景转灰度，透明轮廓与负空间需要单独检查。
- **兼容与引用**：按支持范围导出密度目录中的传统启动图标；项目使用 `roundIcon` 时同时提供对应资源与引用。沿用实际资源名，并给出 `android:icon`、必要时 `android:roundIcon` 的 Manifest 修改片段，避免只交文件却没有引用入口。
- **商店资源**：Google Play 图标单独放在 `store/`，不与自适应前景层或传统启动图标混用。其他 Android 商店按已确定渠道核验，不将 Play 规格称为所有安卓商店统一标准。

制作时复核 [Android 自适应图标](https://developer.android.com/develop/ui/compose/system/icon_design_adaptive) 的图层、安全区和主题行为；当前文档使用 108dp 图层画布与中心 66dp 安全区，关键识别内容要经遮罩检查。按 [Image Asset Studio](https://developer.android.com/studio/write/create-app-icons) 的现行输出或等效可验证流程生成资源与密度。不要把同一张满幅 PNG 作为假前景层覆盖背景，便宣称完成分层适配。

[Google Play 商店图标规范](https://developer.android.com/distribute/google-play/resources/icon-design-specifications) 当前为 512×512、32-bit PNG、sRGB、最大 1024KB；商店会添加圆角和外部投影，交付原稿保持完整方形。每次生产仍复核规范，图内物体光影不等于图标外部投影。

## 3. iOS 套装

按项目实际 Xcode 与图标流程选择一种可接入的原生交付方式，不把旧版固定切图表当成永久标准：

- **资产目录流程**：提供完整 `AppIcon.appiconset/`、图片及有效 `Contents.json`，沿用目标项目的命名和设备支持。用当前 Xcode 模板决定单尺寸还是所需尺寸槽位；不能只列一组 PNG 让开发猜如何配置。按项目支持处理 Any、Dark、Tinted 等外观，注明哪些是自定义素材、哪些由系统生成。
- **Icon Composer 流程**：提供真正由原生工具生成、可打开的 `.icon` 资产以及实际使用的图层素材，核对支持的外观与项目兼容。没有该工具或无法验证时不能把 PNG 改后缀、拼占位目录冒充 `.icon`；在项目支持时交付已验证的资产目录方案，否则标明受阻项。
- **商店与接入**：提供按所用流程准备的 1024×1024 商店用途图或相应可导出资产，并注明上传来源；不假定独立 PNG 可以替代 Xcode 工程图标配置。说明文件复制位置、Target 的图标来源、资产名称或对应构建设置。仅为目标设备和流程生成需要的文件，不默认增加 macOS、watchOS、tvOS 套装。

复核 [Apple App Icons](https://developer.apple.com/design/human-interface-guidelines/app-icons)、[Xcode 资产目录配置](https://developer.apple.com/documentation/xcode/configuring-your-app-icon) 与 [Icon Composer](https://developer.apple.com/documentation/xcode/creating-your-app-icon-using-icon-composer)。Apple 的图标工作流和外观支持可能变化，传统资产目录与分层资产的透明度规则不能混用；按所选路径核对颜色、Alpha、遮罩和外观要求，不把“所有图层不得透明”设成统一限制。

## 4. 包装成开发可使用的文件套装

交付可浏览目录和两个独立压缩包，例如 `app-logo-android-v1.zip`、`app-logo-ios-v1.zip`。下列结构表达文件职责，实际接入路径按工程决定：

```text
app-logo-release-v1/
  android/
    res/                         # 实际图层、XML 和所需密度资源
    store/                       # 已确认商店渠道的独立文件
    source/                      # 本套实际使用的主稿与可用分层素材
    previews/                    # 多种遮罩、主题与真实尺寸预览
    INTEGRATION.md
    FILES.json
    VALIDATION.md
  ios/
    AppIcon.appiconset/           # 或实际可用的 AppIcon.icon，不造空目录
    store/
    source/
    previews/
    INTEGRATION.md
    FILES.json
    VALIDATION.md
  app-logo-android-v1.zip
  app-logo-ios-v1.zip
```

仅创建有实际内容的目录。`FILES.json` 记录相对路径、用途、尺寸或图层角色、适用版本/外观及校验值；同一文件兼具应用和商店用途时可说明复用，不制造无意义副本。`INTEGRATION.md` 用开发能执行的步骤说明复制位置、资源引用、框架生成配置及本地构建/查看方式。`VALIDATION.md` 记录规范查询日期、实际执行的检查与结果，以及缺失工程或工具导致的未验证事项。

## 5. 验收后再报告完成

1. **文件检查**：实际解码图片，核对像素尺寸、编码、颜色、透明度和文件大小；解析 JSON/XML，逐项解析资源引用，检查文件名大小写与重复/缺失资源。压缩后解包检查相对目录、文件清单和校验值一致，无绝对路径、越界路径、系统垃圾文件或占位资源。
2. **视觉检查**：查看真正导出的各平台结果，检查多种遮罩、目标常用尺寸和支持的外观；单色层不能成为实心方块，插画的主体、动作和关系不能被裁掉。实际导出物不通过时修正适配，不能只检查大图或生成提示词。
3. **工程检查**：有可用项目与工具时，完成相应的资源编译/构建、引用核对，以及模拟器或设备上的显示检查。没有工程时明确是独立资源交付；缺少 Xcode、Android SDK 或运行设备时报告准确的验证范围，不用“尺寸正确”代替构建或显示证据。

两套都达到本轮约定的资源交付标准才称双平台资源包完成；否则标为部分完成，列出缺项。资源包完成、已接入代码、构建通过、商店审核通过和产品已发布是不同状态，分别陈述。交付包不默认包含通知图标、启动页、UI 图标、完整 VI 或其他未要求的设计。

规范核对日期：2026-11-07。以上官方链接是下次生产的复核入口，不能用本次快照保证未来平台兼容。
