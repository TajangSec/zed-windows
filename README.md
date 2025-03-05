# Zed
拉取时间：2025/03/05 11:00 GMT+08:00 Asia/Shanghai

Zed的Windows版本，编译方法在https://github.com/zed-industries/zed/blob/main/docs/src/development/windows.md

注：本次构建补充了，cmake 3.31.6、msvc 143的spectre缓解库。

windows构建失败与aws-lc-sys有关，解决方法是注释Cargo.toml里的`debug = "limited"`，解决方法来自[#24791](https://github.com/zed-industries/zed/discussions/24791#discussion-7960013)

我的编译环境（My compilation environment）：

计算机：
```txt
rustc 1.85.0 (4d91de4e4 2025-02-17)

cargo 1.85.0 (d73d2caf9 2024-12-31)

rustup 1.28.0 (6e19fbec7 2025-03-02)

处理器 12th Gen Intel(R) Core(TM) i9-12900H 2.50 GHz

机带 RAM 32.0 GB (31.7 GB 可用)

系统类型 64 位操作系统, 基于 x64 的处理器

版本 Windows 11 专业版

版本 23H2

操作系统版本 22631.4974

体验 Windows 功能体验包 1000.22700.1074.0
```

IDE（VS Code / RustRover）：

VS Code：
```txt
版本: 1.97.2 (user setup)
提交: e54c774e0add60467559eb0d1e229c6452cf8447
日期: 2025-02-12T23:20:35.343Z
Electron: 32.2.7
ElectronBuildId: 10982180
Chromium: 128.0.6613.186
Node.js: 20.18.1
V8: 12.8.374.38-electron.0
OS: Windows_NT x64 10.0.22631
```
RustRover：
```txt
RustRover 2025.1 EAP
Build #RR-251.23774.2, built on March 4, 2025
Source revision: e1b2533d54b2d
授权给 RustRover EAP user: Tajang Wu
到期日期: April 3, 2025
Runtime version: 21.0.6+9-b895.97 amd64 (JCEF 122.1.9)
VM: OpenJDK 64-Bit Server VM by JetBrains s.r.o.
Toolkit: sun.awt.windows.WToolkit
Windows 11.0
GC: G1 Young Generation, G1 Concurrent GC, G1 Old Generation
Memory: 1536M
Cores: 20
Registry:
  ide.balloon.shadow.size=0
  debugger.attach.dialog.enabled=true
  suggest.all.run.configurations.from.context=true
  ide.experimental.ui=true
  terminal.new.ui.show.promotion=true
  transferSettings.vscode.onlyCargoToml=true
  llm.ai.assistant.toolwindow.activation.on.start=false
Non-Bundled Plugins:
  intellij-scheme (0.1.10)
  com.wakatime.intellij.plugin (15.0.3)
  net.seesharpsoft.intellij.plugins.csv (4.0.2)
  com.mallowigi (101.2.0)
```
