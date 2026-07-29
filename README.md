# android-packer
android-packer 是面向应用市场上架、APK报毒的apk加固与资源混淆工具集，提供 Web 界面和 REST API。核心能力：资源隐藏混淆、DEX 加密 + SO 加固 + 壳注入、8 层反调试/反 Frida 等运行时保护。报毒对抗： 壳代码全链路随机化，每次加固生成不同指纹，根除"同壳多 App → 相似度超标"问题；策略分级按渠道裁剪，避免过度加固误报；VirusTotal 扫描阻断 + 安全厂商白名单申诉。上架保障： 华为/小米/OPPO/vivo/Google Play 渠道分级预设，相似度 &lt; 40% 一次过审，多渠道签名隔离防证书污染。支持 Walle/VasDolly 多渠道打包。Python/FastAPI + Vue 3，一键部署 CI/CD。
