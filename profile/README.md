🦀 Ferriscope
==============

Ferriscope is a next-generation Rust-based profiler and binary analysis toolkit — combining static insight with dynamic performance monitoring in one cohesive ecosystem.

------------------------------------------------------------
📦 Repositories
------------------------------------------------------------

ferriscope-core
----------------
The heart of the Ferriscope ecosystem.
A modular Rust library that provides:
- Cross-platform binary parsing (ELF, PE, Mach-O)
- Disassembly and static code inspection
- Control Flow Graph (CFG) and Call Graph generation
- Extensible hooks for dynamic instrumentation
- Shared data models and traits for profiling backends

You can embed ferriscope-core in your own tools for:
- Binary analysis
- Compiler research
- Security auditing
- Custom profilers


ferriscope
----------
The official CLI profiler powered by ferriscope-core.

Features:
- Static Analysis
  Parse and analyze binaries without executing them
  → Inspect sections, symbols, architecture, and code structure

- Dynamic Profiling (WIP)
  Execute binaries safely with runtime data collection
  → Function timing, call counts, memory tracking

- Reports
  Generate rich, readable output (console / JSON / HTML in future)

Planned Features:
- Flamegraph generation
- Real-time sampling profiler
- DWARF & debug symbol integration
- Cross-platform support (Linux, macOS, Windows)

------------------------------------------------------------
🧩 Architecture Overview
------------------------------------------------------------
```
ferriscope/
├── ferriscope-core/    # Core library (binary parsing, disassembly, hooks)
└── ferriscope/         # CLI frontend
```
Core Layer (ferriscope-core)
    Provides static analysis, binary introspection, and common data types.

CLI Layer (ferriscope)
    Handles user commands, report generation, and integrates dynamic runtime analysis.

------------------------------------------------------------
🚀 Getting Started
------------------------------------------------------------

Clone & build:
    git clone https://github.com/ferriscope/ferriscope.git
    cd ferriscope
    cargo build --release

Example usage:
    # Perform static analysis on a binary
    ferriscope analyze ./target_binary

    # Generate JSON report
    ferriscope analyze ./target_binary --output report.json

------------------------------------------------------------
🧱 Dependencies
------------------------------------------------------------

- goblin → Binary parsing
- capstone-rs → Disassembly
- serde / serde_json → Data serialization
- clap → CLI argument parsing

------------------------------------------------------------
🧑‍💻 Contributing
------------------------------------------------------------

Contributions are welcome!
If you’d like to improve Ferriscope, add new analyses, or help with dynamic profiling:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request 🚀

We’re especially looking for:
- Profiling backend developers
- Disassembly / analysis contributors
- UI & visualization enthusiasts

------------------------------------------------------------
⚖️ License
------------------------------------------------------------

Ferriscope is licensed under the MIT License.
You’re free to use, modify, and distribute it, as long as proper attribution is given.

------------------------------------------------------------
💬 Community
------------------------------------------------------------

- Discussions: https://github.com/orgs/ferriscope/discussions
- Issues: https://github.com/ferriscope/ferriscope/issues
- Roadmap: https://github.com/ferriscope/ferriscope/milestones


_Ferriscope — static clarity, dynamic precision._
