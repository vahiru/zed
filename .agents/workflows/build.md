---
description: 编译 Zed 并应用调试补丁
---

1. 检查 Rust 工具链
// turbo
rustc --version
// turbo
cargo --version

2. 如果缺少工具链，请运行项目自带的安装脚本
// turbo
powershell -File script/install-rustup.ps1

3. 编译 Zed 发行版
// turbo
cargo build --release

4. (可选) 导出测试环境变量
// turbo
$env:GPUI_FORCE_D3D_FEATURE_LEVEL="11.0"
// turbo
$env:GPUI_LOG_RENDER_DETAILS="1"

5. 运行 Zed
// turbo
.\target\release\zed.exe
