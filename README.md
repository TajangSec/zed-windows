# Zed
拉取时间：2025/08/23 12:37 GMT+08:00 Asia/Shanghai

Zed的Windows版本，编译方法在https://github.com/zed-industries/zed/blob/main/docs/src/development/windows.md



windows构建失败与aws-lc-sys有关，解决方法是注释Cargo.toml里的`debug = "limited"`，解决方法来自[#24791](https://github.com/zed-industries/zed/discussions/24791#discussion-7960013)

这次遇到一个 `Failed to find fxc.exe`错误，只需要把windows sdk加入到环境变量即可
我的编译环境（My compilation environment）：

计算机：
```txt
rustc 1.89.0 (29483883e 2025-08-04)

cargo 1.89.0 (c24e10642 2025-06-23)

rustup 1.28.2 (e4f3ad6f8 2025-04-28)

处理器 12th Gen Intel(R) Core(TM) i9-12900H 2.50 GHz

机带 RAM 32.0 GB (31.7 GB 可用)

系统类型 64 位操作系统, 基于 x64 的处理器

版本 Windows 11 专业版

版本 24H2

操作系统版本 26100.4770

Windows 功能体验包 1000.26100.197.0
```

IDE（VS Code / RustRover）：

VS Code：
```txt
版本: 1.103.2 (user setup)
提交: 6f17636121051a53c88d3e605c491d22af2ba755
日期: 2025-08-20T16:45:34.255Z
Electron: 37.2.3
ElectronBuildId: 12035395
Chromium: 138.0.7204.100
Node.js: 22.17.0
V8: 13.8.500258-electron.0
OS: Windows_NT x64 10.0.26100
```
RustRover：
```txt
RustRover 2025.2
Build #RR-252.23892.452, built on August 5, 2025
Source revision: 46d96de2d5732
Runtime version: 21.0.7+6-b1038.58 amd64 (JCEF 122.1.9)
VM: OpenJDK 64-Bit Server VM by JetBrains s.r.o.
Toolkit: sun.awt.windows.WToolkit
Windows 11.0
GC: G1 Young Generation, G1 Concurrent GC, G1 Old Generation
Memory: 2048M
Cores: 20
```
