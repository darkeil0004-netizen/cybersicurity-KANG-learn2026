# CyberSecurity KANG Learn 2026

A Rust learning workspace built around a structured set of Rustlings exercises. It helps learners practice Rust fundamentals and progressively explore ownership, data structures, error handling, generics, concurrency, and idiomatic development tools.

## Project Overview

The repository currently contains a single learning project under `05-all-in-one-projects/rustlings`. Each topic is presented as a set of small exercise programs, with corresponding solution examples. The exercises are organized by subject and include quizzes to reinforce concepts along the learning path.

## Repository Structure

```text
.
├── README.md
└── 05-all-in-one-projects/
    └── rustlings/
        ├── Cargo.toml            # Cargo package, binary targets, and Rust/Clippy lints
        ├── rust-analyzer.toml    # rust-analyzer configuration
        ├── .gitignore            # Files excluded from version control
        ├── .rustlings-state.txt  # Rustlings progress state
        ├── exercises/            # Practice tasks grouped by Rust topic
        │   ├── 00_intro/
        │   ├── 01_variables/
        │   ├── 02_functions/
        │   ├── 03_if/
        │   ├── 04_primitive_types/
        │   ├── 05_vecs/
        │   ├── 06_move_semantics/
        │   ├── 07_structs/
        │   ├── 08_enums/
        │   ├── 09_strings/
        │   ├── 10_modules/
        │   ├── 11_hashmaps/
        │   ├── 12_options/
        │   ├── 13_error_handling/
        │   ├── 14_generics/
        │   ├── 15_traits/
        │   ├── 16_lifetimes/
        │   ├── 17_tests/
        │   ├── 18_iterators/
        │   ├── 19_smart_pointers/
        │   ├── 20_threads/
        │   ├── 21_macros/
        │   ├── 22_clippy/
        │   ├── 23_conversions/
        │   └── quizzes/
        └── solutions/             # Example solutions organized like exercises/
            ├── 00_intro/ ... 23_conversions/
            └── quizzes/
```

Each topic folder in `exercises/` contains the corresponding Rust exercise files and, in most cases, a topic-specific README. The `exercises/README.md` maps exercise topics to chapters in *The Rust Programming Language*. `solutions/README.md` explains that solutions demonstrate possible answers; they are examples rather than the only valid implementations.

## Learning Topics

The exercise sequence progresses from introductory syntax to more advanced Rust concepts:

- Variables, functions, conditionals, and primitive types
- Vectors, strings, structs, enums, modules, and hash maps
- Move semantics, options, and error handling
- Generics, traits, and lifetimes
- Tests, iterators, smart pointers, and threads
- Macros, Clippy, and type conversions
- Review quizzes

## Technologies

- **Language:** Rust (the Cargo manifest specifies the 2024 edition)
- **Build and package tooling:** Cargo
- **Editor support:** rust-analyzer configuration
- **Code quality:** Rust compiler lints and Clippy lints configured in `Cargo.toml`
- **Dependencies:** The manifest defines exercise binaries and package/lint settings; no third-party dependencies are listed.

The manifest registers exercise and solution files as separate Cargo binaries, allowing individual tasks to be compiled and run by name. It also forbids unsafe code and unstable features for the exercises and configures selected Clippy checks.

## Getting Started

Install a Rust toolchain that supports the 2024 edition, then enter the Rustlings project directory:

```bash
cd 05-all-in-one-projects/rustlings
```

Run an exercise binary by its name as declared in `Cargo.toml`:

```bash
cargo run --bin intro1
cargo run --bin variables1
```

Build the Cargo package with:

```bash
cargo build
```

Run Cargo's test targets with:

```bash
cargo test
```

To explore, start with the matching exercise folder and its README, attempt the task in `exercises/`, then compare your work with the corresponding example in `solutions/`.

## Intended Audience

This repository is suitable for Rust beginners and learners who want structured, hands-on practice. It is an educational workspace, not a deployed application or service.
