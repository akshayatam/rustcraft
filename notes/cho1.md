# 🦀 Rust Chapter 1 – Getting Started (Key Notes)

## 📌 What You Learn
- How to install Rust
- How to write and run a basic Rust program
- How to use Cargo (Rust’s build system and package manager)

---

## ⚙️ Installation

### Install Rust using rustup
```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

### Verify installation
```bash
rustc --version
```

### Update Rust
```bash
rustup update
```

### Uninstall Rust
```bash
rustup self uninstall
```

### Notes
- Rust is installed via rustup, which manages versions
- A linker is required (comes with C compiler like GCC or MSVC)
- Documentation can be accessed locally:

```bash
rustup doc
```

---

## 👋 Hello World Program

### Basic Rust Program
```rust
fn main() {
    println!("Hello, world!");
}
```

### Key Concepts
- `fn main()` → entry point of every Rust program
- `println!` → macro (not a function)
- `!` → indicates macro usage
- `;` → ends statements

---

## ▶️ Compile and Run (Without Cargo)

### Compile
```bash
rustc main.rs
```

### Run
```bash
./main      # Linux/macOS
.\main      # Windows
```

### Important
- Rust is an ahead-of-time compiled language
- Compilation and execution are separate steps

---

## 📦 Cargo (Rust Build System)

### Check Cargo
```bash
cargo --version
```

### Create New Project
```bash
cargo new hello_cargo
cd hello_cargo
```

### Project Structure
```bash
hello_cargo/
├── Cargo.toml
└── src/
    └── main.rs
```

---

## 🧾 Cargo.toml Basics
```bash
[package]
name = "hello_cargo"
version = "0.1.0"
edition = "2024"

[dependencies]
```
- `[package]` → project metadata
- `[dependencies]` → external libraries (crates)

---

## 🛠️ Cargo Commands

### Build
```bash
cargo build
```

### Run
```bash
cargo run
```

### Check (fast compile without binary)
```bash
cargo check
```

### Release Build (optimized)
```bash
cargo build --release
```

---

## ⚡  Why Cargo Matters
- Handles builds automatically
- Manages dependencies
- Standardizes project structure
- Works the same across all OS

---

## 🧠 Key Takeaways
- Rust uses compilation before execution
- `rustc` is fine for small programs
- Cargo is used for real-world projects
- Rust programs start from `main()`
- Macros (`!`) are an important Rust feature
