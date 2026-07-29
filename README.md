# android-packer
android-packer 是一个面向应用市场上架的 Android APK 加固与资源混淆工具集，提供 Web 可视化操作界面和 REST API。核心能力包括：资源路径缩短与文件名混淆甚至隐藏；DEX 加密 + SO 库加固 + 壳注入；多层运行时保护（8 层反调试、反 Frida、反 Xposed、反 Hook、模拟器检测、完整性校验、Merkle 哈希树）。

## 报毒对抗体系
🛡️ 报毒对抗体系： 内置六层报毒与相似度解决方案——① 壳代码全链路随机化（smali 包名/类名/方法名随机化、SO 导出符号与字符串表混淆、注入组件名随机化、assets 文件指纹优化），每次加固生成指纹完全不同的壳，从根本上消除"同一壳被多 App 共用导致相似度 > 80%"的报毒根因；② 策略分级（minimal / standard / maximum），按渠道裁剪保护项，避免过度加固触发误报——Google Play 仅混淆不注入壳，国内大厂市场启用轻量 DEX 加密跳过反调试，第三方下载站才开启全保护；③ VirusTotal 发版前自动扫描，报毒引擎 ≥ 3 阻断发布，配合 360/腾讯/华为/小米等主流安全厂商白名单申诉通道；④ 签名合规（正式证书 + V1+V2+V3 全量签名，杜绝 debug 签名出厂）。

## 应用上架
🏪 应用市场上架保障： 针对华为、小米、OPPO、vivo、Google Play 等主流市场差异化的审核策略，内置渠道分级加固预设，在保护强度与上架成功率间取得平衡——资源混淆 + ProGuard/R8 代码混淆搭配轻量 DEX 加密，确保相似度检测 < 40% 一次过审；随机壳变体杜绝多 App 代码指纹雷同；多渠道签名隔离防止证书污染扩散；配套各市场误报申诉 SOP 与自动化 CI/CD 加固流水线。

## 多渠道打包
📦 多渠道打包： 支持 Walle / VasDolly / Manifest meta-data 三种渠道注入方式，加固阶段一步完成。

## 部署集成
基于 Python/FastAPI + Vue 3 构建，支持一键部署，可集成至 CI/CD 流水线。

# 联系方式
## telegram
[@apk_gongfang]([https://www.baidu.com](https://t.me/apk_gongfang) "APK工坊")
