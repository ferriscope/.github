# 🦀 Ferriscope

> **Ferriscope** is a next-generation Rust-based profiler and binary analysis toolkit — combining *static insight* with *dynamic performance monitoring* in one cohesive ecosystem.

---

## 📦 Repositories

### [`ferriscope-core`](https://github.com/ferriscope/ferriscope-core)
The heart of the Ferriscope ecosystem.  
A modular Rust library that provides:
- Cross-platform **binary parsing** (ELF, PE, Mach-O...etc)
- **Disassembly** and static code inspection
- **Control Flow Graph (CFG)** and **Call Graph** generation
- Extensible hooks for **dynamic instrumentation**
- Shared data models and traits for profiling backends

You can embed `ferriscope-core` in your own tools for:
- Binary analysis  
- Compiler research  
- Security auditing  
- Custom profilers

---

### [`ferriscope`](https://github.com/ferriscope/ferriscope)
The official CLI profiler powered by `ferriscope-core`.

#### 🔧 Features
- 🔍 **Static Analysis**  
  Parse and analyze binaries without executing them  
  → Inspect sections, symbols, architecture, and code structure  

- ⚡ **Dynamic Profiling** *(WIP)*  
  Execute binaries safely with runtime data collection  
  → Function timing, call counts, memory tracking  

- 📊 **Reports**  
  Generate rich, readable output (console / JSON / HTML in future)

#### 🧠 Planned Features
- Flamegraph generation  
- Real-time sampling profiler  
- DWARF & debug symbol integration  
- Cross-platform support (Linux, macOS, Windows)  

---

## 🧩 Architecture Overview
```
ferriscope/
├── ferriscope-core/ # Core library (binary parsing, disassembly, hooks)
└── ferriscope/ # CLI frontend
```
- **Core Layer (`ferriscope-core`)**  
  Provides static analysis, binary introspection, and common data types.

- **CLI Layer (`ferriscope`)**  
  Handles user commands, report generation, and integrates dynamic runtime analysis.

---

## 🚀 Getting Started

### Clone & build
```bash
git clone https://github.com/ferriscope/ferriscope.git
cd ferriscope
cargo build --release
```
