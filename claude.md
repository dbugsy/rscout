# Learning Rust - A Systems Programming Journey

## About This Learning Path

This is a project-based Rust learning curriculum designed for an experienced software engineer (Ruby/TypeScript/Java background) to understand low-level systems concepts, memory management, and build real-world tools.

## Learning Philosophy

- **Project-driven**: Build a real CLI tool with web components
- **Socratic method**: Learn through guided problem-solving, not copy-paste
- **Incremental complexity**: Start simple, add features progressively
- **Deep understanding**: Focus on WHY Rust works this way, not just HOW

---

## Phase 1: Rust Fundamentals & The Ownership Model

### Topics to Cover

#### 1.1 Setup & Tooling
- [ ] Install Rust (rustup, cargo)
- [ ] Understand cargo workspace
- [ ] Basic project structure
- [ ] cargo commands: build, run, test, check

#### 1.2 Syntax Basics (Quick - You Know Programming)
- [ ] Variables and mutability (let vs let mut)
- [ ] Basic types (integers, floats, bool, char)
- [ ] Functions and return values
- [ ] Control flow (if/else, loop, while, for)
- [ ] Pattern matching (match expressions)

#### 1.3 The Core Concept: Ownership ⭐
**This is what makes Rust different from Ruby/TypeScript**

- [ ] **Ownership rules**: Each value has ONE owner
- [ ] **Move semantics**: Understanding when values move vs copy
- [ ] **Borrowing**: References (&T) and mutable references (&mut T)
- [ ] **Lifetimes**: Why references need lifetime annotations
- [ ] **The borrow checker**: Your new best friend/enemy

**Why this matters**:
- Ruby: Garbage collector handles memory
- TypeScript: JavaScript GC handles memory
- Rust: Compiler ensures memory safety at compile time (no GC!)

#### 1.4 Common Collections
- [ ] Vec<T> (like Ruby Array, but typed)
- [ ] String vs &str (crucial distinction)
- [ ] HashMap<K, V>
- [ ] Understanding heap vs stack allocation

---

## Phase 2: Error Handling & Type System

### Topics to Cover

#### 2.1 Result and Option Types
- [ ] Option<T>: Handling null without null
- [ ] Result<T, E>: Explicit error handling
- [ ] The ? operator for error propagation
- [ ] Pattern matching on Results/Options

**Comparison**:
- Ruby: Exceptions, nil values
- TypeScript: try/catch, undefined/null
- Rust: Explicit Result types, no exceptions

#### 2.2 Structs and Enums
- [ ] Defining structs (like Ruby classes, but no inheritance)
- [ ] Methods and associated functions (impl blocks)
- [ ] Enums (more powerful than TypeScript unions)
- [ ] Enum variants with data

#### 2.3 Traits
- [ ] What traits are (like Ruby modules/TypeScript interfaces)
- [ ] Implementing traits
- [ ] Trait bounds
- [ ] Common traits: Debug, Clone, Copy, Display

---

## Phase 3: Real Systems Concepts

### Topics to Cover

#### 3.1 Memory Deep Dive
- [ ] Stack vs Heap allocation
- [ ] When copying happens (Copy trait)
- [ ] When cloning happens (Clone trait)
- [ ] Smart pointers: Box<T>, Rc<T>, Arc<T>
- [ ] Interior mutability: RefCell<T>

#### 3.2 Concurrency & Parallelism
- [ ] Threads and thread safety
- [ ] Send and Sync traits
- [ ] Channels for message passing
- [ ] Shared state with Mutex/RwLock
- [ ] async/await (if needed for web)

**Why Rust shines here**:
- Fearless concurrency - compiler prevents data races
- No GC pauses during concurrent operations

---

## Phase 4: Building Real Tools

### Topics to Cover

#### 4.1 CLI Development
- [ ] Argument parsing (clap crate)
- [ ] File I/O and error handling
- [ ] Working with stdin/stdout
- [ ] Environment variables
- [ ] Exit codes and signals

#### 4.2 Working with External Crates
- [ ] Understanding Cargo.toml dependencies
- [ ] Reading crate documentation
- [ ] Common utility crates (serde, anyhow, thiserror)

#### 4.3 Web Development (Optional/Later)
- [ ] HTTP concepts in Rust
- [ ] Web frameworks (axum, actix-web)
- [ ] Serialization with serde
- [ ] Database integration

---

## The Project: rscout - Network Reconnaissance Scanner

**Status**: Planning Complete - Ready to Build

A high-performance network scanner built for CTF competitions and security research. See `PROJECT.md` for full details.

### Core Features:
- TCP port scanning (fast, concurrent)
- Service detection and banner grabbing
- Multiple output formats (text, JSON)
- CLI with progress indicators
- Configurable scan parameters
- Real-world CTF usability

### Why This Project is Perfect for Learning:
1. **Network programming**: TCP/IP, sockets, protocols
2. **Async/concurrency**: tokio, parallel scanning
3. **Memory management**: Buffers, efficient data structures
4. **Error handling**: Network errors, timeouts, parsing
5. **CLI development**: Real tool you'll actually use
6. **Performance critical**: Speed matters in CTFs

### Task Tracking:
All learning tasks are defined in `TASKS.md` - 30 core tasks organized into sprints, each teaching specific Rust concepts while building real features.

### Current Sprint: Sprint 0 - Setup
### Next Task: TASK-001 - Install Rust Toolchain

---

## Learning Resources

### Essential Reading
- [The Rust Book](https://doc.rust-lang.org/book/) - Official guide
- [Rust By Example](https://doc.rust-lang.org/rust-by-example/) - Code examples
- [Rustlings](https://github.com/rust-lang/rustlings) - Small exercises

### For Systems Understanding
- [The Rustonomicon](https://doc.rust-lang.org/nomicon/) - Unsafe Rust (later)
- [Rust for Rustaceans](https://rust-for-rustaceans.com/) - Intermediate/advanced

### Quick References
- [Rust Cheat Sheet](https://cheats.rs/) - Syntax and patterns
- [std library docs](https://doc.rust-lang.org/std/) - Standard library

---

## Progress Tracking

We'll track progress using structured tasks that will be created as we go.

### Current Phase: Setup
### Next Steps: Install Rust toolchain and create first "Hello, World" program

---

## Notes Section

_Add notes, insights, and "aha!" moments as you learn_

### Key Insights
-

### Challenges & Solutions
-

### Questions for Later
-
