# atttescore

> ⚠️ **Note / 注意**  
> This project is still in development. Please use with caution.  
> 本專案仍在開發中，請小心使用。

---

## Introduction / 專案介紹

**atttescore** is the core execution engine for `attesintel`.  
It handles CPU emulation, ARM64 instruction decoding, and execution.

**atttescore** 是 `attesintel` 的核心引擎，  
負責 CPU 模擬、ARM64 指令解碼與執行。

It is intended for educational and research purposes.  
Future plans include GUI support, JIT execution, and extended instruction coverage.

本專案主要用於學習與研究，  
未來將加入 GUI 支援、JIT 執行與更完整的指令集。

---

## Project Status / 專案狀態

**Version:** 3.0 Beta  
**Status:** Experimental / Research Stage

- Not production-ready  
- Not a full Rosetta replacement  
- Intended for educational use only  

- 尚未達到正式穩定版  
- 並非 Rosetta 替代品  
- 僅供學習與研究用途  

---

## Core Features / 核心功能

### CPU & Execution Core / CPU 與執行核心
- ARM64 CPU state emulation (x0–x30, SP, PC)  
- Instruction fetch → decode → execute loop  
- Stack and register tracking  

- ARM64 CPU 狀態模擬（x0–x30、SP、PC）  
- 指令擷取 → 解碼 → 執行流程  
- 堆疊與暫存器狀態追蹤  

### Instruction Support (Growing) / 指令集支援（持續擴充）
- Arithmetic: ADD, SUB, MOV  
- Control flow: B, BL, RET  
- Memory: LDR, STR, STP, LDP  
- System: SVC (syscall entry)  

- 算術：ADD、SUB、MOV  
- 控制流程：B、BL、RET  
- 記憶體：LDR、STR、STP、LDP  
- 系統：SVC（系統呼叫入口）  

### Mach-O Support / Mach-O 支援
- ARM64 Mach-O parsing  
- Entry point (`LC_MAIN`) loading  
- Basic memory mapping  

- ARM64 Mach-O 檔案解析  
- 程式進入點（LC_MAIN）  
- 基本記憶體映射  

### System Call Framework / 系統呼叫框架
- Minimal syscall handler  
- CLI I/O foundation  
- Expandable syscall table  

- 最小化 syscall 處理器  
- CLI 輸入輸出基礎  
- 可擴充 syscall 對照表  

---

## What atttescore is NOT / 本專案不是什麼

- ❌ Not a full macOS compatibility layer  
- ❌ Not a security bypass tool  
- ❌ Not guaranteed to run complex commercial apps  

- ❌ 不是完整 macOS 相容層  
- ❌ 不是安全繞過工具  
- ❌ 不保證可執行大型商業 App  

---

## Build Instructions / 編譯方式

bash
clang src/*.c -Iinclude -o atttescore
Test with a minimal ARM64 binary or assembly output.
可搭配簡單 ARM64 組合語言或測試程式進行測試。

Roadmap / 開發方向
 Extend ARM64 instruction coverage

 Improve syscall compatibility

 Memory protection & MMU model

 JIT / block execution

 GUI & framebuffer output

 擴充 ARM64 指令集支援

 強化 syscall 相容性

 記憶體保護與 MMU 模型

 JIT / 區塊執行

 GUI 與 framebuffer 輸出

---

License / 授權
This project is licensed under the Apache License 2.0.
You may use, modify, and distribute this software in accordance with the license.

本專案採用 Apache License 2.0 授權。
你可以依授權規範使用、修改與散布本專案。

---

Disclaimer / 免責聲明
This software is provided "AS IS", without warranty of any kind.
Use at your own risk.

本軟體以「現況提供」，不附帶任何形式之保證，
使用風險請自行承擔。

Author
Created by junwei
Experimental system software & architecture research

---
