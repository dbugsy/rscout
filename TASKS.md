# rscout - Learning Tasks (ADHD-Optimized Format)

## HOW TO USE THIS TASK LIST

### Understanding the 15-Minute Task Format

**What is a "15-minute task"?**
- 15 minutes of FOCUSED work on ONE specific deliverable
- Not "work for 15 minutes then stop" - it's "this should take about 15 focused minutes"
- If you're hyperfocused, you might finish in 10 minutes - that's great!
- If you're low-energy, it might take 20 minutes - that's also okay

**Every sub-task has:**
- **ONE clear action** (e.g., "Create a function that...")
- **DONE = criteria** (exactly what "finished" means)
- **BREAK after this** (directive to take a break, not a suggestion)

### Working with Your Energy Levels

**Start of each session:**
1. Check your energy: High / Medium / Low
2. High energy = You might do 4-6 sub-tasks before a real break
3. Low energy = Do 1 sub-task, take break, assess if you continue

**During hyperfocus:**
- The "BREAK after this" directive is IMPORTANT
- Stand up, look away from screen, drink water (2 minutes minimum)
- You can continue after the break, but TAKE THE BREAK
- This prevents burnout and maintains retention

**During low energy:**
- Do ONE sub-task
- Take a real break (5-10 minutes)
- Be honest: Do I have energy for another? If not, STOP and celebrate what you did

### The Stuck Protocol

**If stuck for 30 minutes on a sub-task:**
1. Ask for Socratic guidance: "I'm stuck on TASK-XXXy - can you guide me with questions?"
2. I will NOT give you the answer - I'll ask questions to help you discover it
3. Expect questions like: "What is the compiler telling you?" "What do you predict will happen?"
4. If still stuck after 30 more minutes: Move to next sub-task, mark this one for later

**Remember:**
- I use the Socratic method - I guide with questions, not answers
- Compiler errors are learning opportunities
- "I don't know" is a valid answer - it tells us what to explore

### Sub-task Completion

**Mark sub-tasks complete when:**
- You have working code that compiles (if it's a coding task), OR
- You can explain the concept in writing (if it's a learning task)

**Don't mark complete if:**
- Code has errors you don't understand
- You copy-pasted without understanding
- You "made it work" but don't know why

### Sprint Metadata Guide

Each sprint shows:
- **Total sub-tasks**: How many 15-min chunks
- **Sequential time**: If doing back-to-back (with breaks)
- **Completion modes**:
  - "1 hyperfocus session" = 2-3 hours of focused work
  - "Spread across X days" = doing 1-3 sub-tasks per day

---

## SPRINT 0: Setup & Environment

**Sprint Metadata:**
- Total sub-tasks: 7
- Sequential time: ~2 hours (with breaks)
- Could complete in: 1 focused session OR spread across 1-2 days

---

### TASK-001: Install Rust Toolchain

**Total Time:** ~45 minutes (3 sub-tasks × 15 min)

#### Sub-task 001a: Install rustup (15 min)
**Your Task:**
- Go to https://rustup.rs/
- Run the installation command
- Follow the installer prompts (use defaults)
- Let the installer complete

**DONE =**
- Terminal shows "Rust is installed now" message
- You can close and reopen terminal

**BREAK after this** (2 minutes - stand up, stretch)

---

#### Sub-task 001b: Verify installation (15 min)
**Your Task:**
- Open a NEW terminal window (important!)
- Run: `rustc --version`
- Run: `cargo --version`
- Run: `rustup --version`
- Take a screenshot or copy the version numbers

**DONE =**
- All three commands show version numbers (1.70+)
- No "command not found" errors

**BREAK after this**

---

#### Sub-task 001c: Hello World verification (15 min)
**Your Task:**
- Create a temporary directory (anywhere): `mkdir ~/rust-test`
- `cd ~/rust-test`
- Create file: `hello.rs`
- Write this code:
  ```rust
  fn main() {
      println!("Hello, Rust!");
  }
  ```
- Compile: `rustc hello.rs`
- Run: `./hello`

**DONE =**
- Compiles without errors
- Prints "Hello, Rust!" when you run it
- You can explain what `fn main()` and `println!` do

**BREAK after this** (5 minutes - celebrate! You compiled Rust!)

**Reflection Question:** How is this different from running Ruby or TypeScript? (Write 2-3 sentences)

---

### TASK-002: Create rscout Project

**Total Time:** ~45 minutes (3 sub-tasks × 15 min)

#### Sub-task 002a: Create project with cargo (15 min)
**Your Task:**
- Navigate to your projects directory: `cd ~/projects/learnRust`
- Run: `cargo new rscout`
- Look at what was created: `ls -la rscout/`
- Open the project in your editor

**DONE =**
- Directory `rscout/` exists
- Contains: `Cargo.toml`, `src/main.rs`, `.git/` (cargo inits git automatically)
- You can open it in your editor

**BREAK after this**

---

#### Sub-task 002b: Understand project structure (15 min)
**Your Task:**
- Read `Cargo.toml` - what's in it?
- Read `src/main.rs` - what does it do?
- Run: `cargo build`
- Run: `cargo run`
- Look in `target/debug/` - what's there?

**DONE =**
- You can explain what `Cargo.toml` contains (package name, version, dependencies)
- You understand `src/main.rs` is the entry point
- Program prints "Hello, world!"
- You know `target/` contains build artifacts

**BREAK after this**

**Socratic Checkpoint:** I'll ask you: "Why is there a `target/` directory? What's in it?"

---

#### Sub-task 002c: Learn cargo commands (15 min)
**Your Task:**
- Run: `cargo check` (what does this do?)
- Run: `cargo build --release` (how is this different?)
- Run: `cargo clean` (what happens to target/?)
- Run: `cargo run` again

**DONE =**
- You can explain the difference between:
  - `cargo check` (fast compile check, no binary)
  - `cargo build` (debug build)
  - `cargo build --release` (optimized build)
  - `cargo run` (build + run)

**BREAK after this** (5 minutes)

**Reflection Question:** When would you use `cargo check` vs `cargo build`? Why?

---

### TASK-003: First Git Commit

**Total Time:** ~30 minutes (2 sub-tasks × 15 min)

#### Sub-task 003a: Review what cargo created (15 min)
**Your Task:**
- Run: `git status` (inside rscout/)
- Notice cargo already ran `git init`
- Look at what's being tracked
- Run: `cat .gitignore` - what's in there?

**DONE =**
- You understand cargo created a git repo automatically
- `.gitignore` includes `/target/` (build artifacts)
- You know why we ignore `target/`

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why do we ignore the target/ directory? What would happen if we committed it?"

---

#### Sub-task 003b: Make first commit (15 min)
**Your Task:**
- `git add .`
- `git commit -m "Initial rscout project created with cargo"`
- Run: `git log` to see your commit

**DONE =**
- Commit exists with message
- `git status` shows "working tree clean"
- You can see the commit in git log

**BREAK after this** (5 minutes - Sprint 0 complete!)

**Sprint 0 Complete!** You have:
- Working Rust toolchain
- Created a Rust project
- Committed it to git
- Understanding of cargo basics

---

## SPRINT 1: Rust Fundamentals

**Sprint Metadata:**
- Total sub-tasks: 18
- Sequential time: ~5 hours (with breaks)
- Could complete in: 2 hyperfocus sessions OR spread across 3-5 days

---

### TASK-004: Variables and Mutability Exercise

**Total Time:** ~60 minutes (4 sub-tasks × 15 min)

#### Sub-task 004a: Immutable variable experiment (15 min)
**Your Task:**
- Open `src/main.rs`
- Delete the "Hello, world!" code
- Write this code:
  ```rust
  fn main() {
      let port = 8080;
      println!("Port: {}", port);
  }
  ```
- Run: `cargo run`

**DONE =**
- Code compiles
- Prints: "Port: 8080"
- You understand `let` creates an immutable binding

**BREAK after this**

---

#### Sub-task 004b: Try to mutate - observe error (15 min)
**Your Task:**
- Add a line after `let port = 8080;`:
  ```rust
  port = 9090;  // Try to change it
  ```
- Run: `cargo build`
- READ the compiler error message carefully
- Don't fix it yet - just read the error

**DONE =**
- Compiler gives error: "cannot assign twice to immutable variable"
- You can quote the error message
- You understand WHY it failed

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "What is the compiler telling you? Why doesn't Rust allow this by default?"

---

#### Sub-task 004c: Fix with mutable variable (15 min)
**Your Task:**
- Change the line to: `let mut port = 8080;`
- Keep the `port = 9090;` line
- Compile and run
- Observe that it works now

**DONE =**
- Code compiles without errors
- You can explain the difference between `let` and `let mut`
- You understand Rust is immutable by default

**BREAK after this**

---

#### Sub-task 004d: Experiment with multiple variables (15 min)
**Your Task:**
- Create 3 variables:
  1. `target_ip` (immutable, value: "127.0.0.1")
  2. `timeout_ms` (mutable, initial value: 1000)
  3. `max_ports` (immutable, value: 1000)
- Change `timeout_ms` to 2000
- Try to change `max_ports` (should fail)
- Print all three variables

**DONE =**
- Code compiles with the mutable change
- Fails when trying to change immutable variable
- All three variables print correctly

**BREAK after this** (5 minutes)

**Reflection Question:** Why would Rust make immutability the default? What problems does this prevent? (Compare to Ruby/TypeScript)

---

### TASK-005: Functions and Return Values

**Total Time:** ~90 minutes (6 sub-tasks × 15 min)

#### Sub-task 005a: Create first function (15 min)
**Your Task:**
- Below `main()`, create this function:
  ```rust
  fn is_valid_port(port: u16) -> bool {
      port >= 1 && port <= 65535
  }
  ```
- In `main()`, call it: `println!("Valid: {}", is_valid_port(8080));`
- Run the code

**DONE =**
- Code compiles
- Prints: "Valid: true"
- You understand the syntax: `fn name(param: Type) -> ReturnType`

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why is there no `return` keyword? Why use `u16` for port?"

---

#### Sub-task 005b: Test with invalid ports (15 min)
**Your Task:**
- Test your function with: 0, 1, 80, 65535, 65536
- Print the results for each
- Observe what happens with 65536

**DONE =**
- You get a compiler error for 65536
- You understand `u16` can only hold 0-65535
- Tests for other values work correctly

**BREAK after this**

---

#### Sub-task 005c: Introduce Option<T> concept (15 min)
**Your Task:**
- Read this example (don't write it yet):
  ```rust
  fn parse_port(input: &str) -> Option<u16> {
      input.parse().ok()
  }
  ```
- Research: What is `Option<T>`?
- Look up: What does `.ok()` do?

**DONE =**
- You can explain `Option<T>` is either `Some(value)` or `None`
- You understand this is Rust's way of handling "no value" (instead of null)
- You know `.ok()` converts `Result` to `Option`

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "How is Option different from null in TypeScript? Why is this safer?"

---

#### Sub-task 005d: Write parse_port function (15 min)
**Your Task:**
- Write the `parse_port` function (from 005c)
- In `main()`, try parsing "8080"
- Print the result

**DONE =**
- Code compiles
- Prints: `Some(8080)`
- You understand the function returns `Option<u16>`

**BREAK after this**

---

#### Sub-task 005e: Handle None case with match (15 min)
**Your Task:**
- Parse "invalid" string
- Use `match` to handle both cases:
  ```rust
  match parse_port("invalid") {
      Some(port) => println!("Port: {}", port),
      None => println!("Invalid port"),
  }
  ```

**DONE =**
- Code compiles
- Prints "Invalid port" for invalid input
- You understand `match` must handle all cases (exhaustive)

**BREAK after this**

---

#### Sub-task 005f: Combine validation and parsing (15 min)
**Your Task:**
- Write a function: `fn get_valid_port(input: &str) -> Option<u16>`
- It should parse AND validate (1-65535)
- Test with: "80", "0", "70000", "invalid"

**DONE =**
- Function returns `Some(port)` only for valid ports
- Returns `None` for invalid input or out-of-range
- You combined `parse_port` and `is_valid_port` logic

**BREAK after this** (5 minutes)

**Reflection Question:** How does Option<T> + match prevent null pointer errors? Write 2-3 sentences.

---

### TASK-006: Structs for Scan Configuration

**Total Time:** ~90 minutes (6 sub-tasks × 15 min)

#### Sub-task 006a: Define ScanConfig struct (15 min)
**Your Task:**
- Above `main()`, define:
  ```rust
  struct ScanConfig {
      target_ip: String,
      start_port: u16,
      end_port: u16,
      timeout_ms: u64,
  }
  ```
- In `main()`, try to create an instance (you'll need to figure out the syntax)

**DONE =**
- Struct is defined
- You successfully create an instance with values
- Code compiles

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why use `String` instead of `&str` here? What's the difference?"

---

#### Sub-task 006b: Create a new() function (15 min)
**Your Task:**
- Create an associated function (like a constructor):
  ```rust
  impl ScanConfig {
      fn new(target_ip: String, start_port: u16, end_port: u16, timeout_ms: u64) -> Self {
          // Fill this in
      }
  }
  ```
- Use it in `main()` to create a config

**DONE =**
- `new()` function returns a `ScanConfig`
- You can create config: `let config = ScanConfig::new(...);`
- You understand `Self` refers to `ScanConfig`

**BREAK after this**

---

#### Sub-task 006c: Add a method that uses &self (15 min)
**Your Task:**
- Add a method to print the config:
  ```rust
  fn print(&self) {
      println!("Target: {}", self.target_ip);
      // Add the other fields
  }
  ```
- Call it: `config.print();`

**DONE =**
- Method prints all fields
- You understand `&self` means "borrow this instance"
- You can call it with dot notation

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "What's the difference between `new()` (no self) and `print(&self)`?"

---

#### Sub-task 006d: Add validation method (15 min)
**Your Task:**
- Add method: `fn is_valid(&self) -> bool`
- Should check:
  - `start_port` <= `end_port`
  - `end_port` > 0
  - `timeout_ms` > 0
- Test with valid and invalid configs

**DONE =**
- Validation method returns correct bool
- You tested both valid and invalid configurations
- Code compiles and runs

**BREAK after this**

---

#### Sub-task 006e: Experiment with mutating methods (15 min)
**Your Task:**
- Try to add: `fn set_timeout(&self, new_timeout: u64)`
- Try to implement: `self.timeout_ms = new_timeout;`
- Observe compiler error
- Fix by changing to `&mut self`

**DONE =**
- You got error with `&self` (cannot mutate)
- You fixed it with `&mut self`
- You understand when to use `&mut self` vs `&self`

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why did you need `&mut self`? What is the difference from `&self`?"

---

#### Sub-task 006f: Create a builder-style method (15 min)
**Your Task:**
- Add method: `fn with_timeout(mut self, timeout_ms: u64) -> Self`
- It should set the timeout and return `self`
- Try chaining: `ScanConfig::new(...).with_timeout(5000)`

**DONE =**
- Method takes ownership (`self`, not `&self`)
- Returns modified instance
- You can chain method calls
- You understand this consumes the original instance

**BREAK after this** (5 minutes)

**Reflection Question:** When would you use `&self` vs `&mut self` vs `self`? Give an example for each.

---

### TASK-007: Enums for Scan Results

**Total Time:** ~60 minutes (4 sub-tasks × 15 min)

#### Sub-task 007a: Define PortState enum (15 min)
**Your Task:**
- Define enum:
  ```rust
  enum PortState {
      Open,
      Closed,
      Filtered,
      Unknown,
  }
  ```
- Create a variable with each variant
- Try to print them (will fail - that's expected)

**DONE =**
- Enum defined with 4 variants
- You created instances: `let state = PortState::Open;`
- You understand you can't print without implementing a trait

**BREAK after this**

---

#### Sub-task 007b: Match on PortState (15 min)
**Your Task:**
- Write a function: `fn state_to_string(state: PortState) -> String`
- Use `match` to convert each variant to a string
- Test it with different states

**DONE =**
- Match handles all four cases
- Returns appropriate string for each
- Compiler enforces exhaustive matching

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "What happens if you forget a match arm? Why does Rust require this?"

---

#### Sub-task 007c: Create ScanResult struct (15 min)
**Your Task:**
- Define:
  ```rust
  struct ScanResult {
      port: u16,
      state: PortState,
  }
  ```
- Create a few instances
- Try to print them

**DONE =**
- Struct combines port number with state
- You created instances successfully
- You understand this models a "scan result"

**BREAK after this**

---

#### Sub-task 007d: Add method to format results (15 min)
**Your Task:**
- Add to `impl ScanResult`:
  ```rust
  fn format(&self) -> String {
      // Return something like "Port 80: Open"
  }
  ```
- Use `state_to_string` from 007b
- Test with different results

**DONE =**
- Method returns formatted string
- Works for all port states
- You're combining struct + enum + methods

**BREAK after this** (5 minutes)

**Reflection Question:** How are enums in Rust different from TypeScript unions or Java enums?

---

### TASK-008: Error Handling with Result

**Total Time:** ~90 minutes (6 sub-tasks × 15 min)

#### Sub-task 008a: Understand Result<T, E> (15 min)
**Your Task:**
- Read about `Result<T, E>` in Rust docs
- Try this code:
  ```rust
  fn divide(a: i32, b: i32) -> Result<i32, String> {
      if b == 0 {
          Err("Division by zero".to_string())
      } else {
          Ok(a / b)
      }
  }
  ```
- Test with different inputs

**DONE =**
- You understand Result is either `Ok(value)` or `Err(error)`
- Function compiles and works
- You can explain when to use Result vs Option

**BREAK after this**

---

#### Sub-task 008b: Create custom error type (15 min)
**Your Task:**
- Define:
  ```rust
  enum ScanError {
      InvalidPort,
      InvalidIpAddress,
      InvalidRange,
  }
  ```
- Update validation functions to return `Result<(), ScanError>`

**DONE =**
- Custom error enum defined
- At least one function returns `Result` with your error type
- Code compiles

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why create a custom error type instead of using String?"

---

#### Sub-task 008c: Use match on Result (15 min)
**Your Task:**
- Call a function that returns `Result`
- Match on the result:
  ```rust
  match some_validation() {
      Ok(()) => println!("Valid!"),
      Err(e) => println!("Error: {:?}", e),
  }
  ```
- Test both success and error cases

**DONE =**
- Match handles both Ok and Err
- Error case prints the error (using Debug trait)
- You understand Result forces you to handle errors

**BREAK after this**

---

#### Sub-task 008d: Learn the ? operator (15 min)
**Your Task:**
- Create function that calls multiple validations:
  ```rust
  fn validate_config(config: &ScanConfig) -> Result<(), ScanError> {
      validate_ports(config)?;
      validate_ip(config)?;
      Ok(())
  }
  ```
- Understand what `?` does (early return on error)

**DONE =**
- You understand `?` propagates errors
- Function returns first error encountered, or Ok(())
- You know this is shorthand for match + return

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "What does the ? operator do? How is it different from unwrap()?"

---

#### Sub-task 008e: Implement validation functions (15 min)
**Your Task:**
- Implement `validate_ports()` - checks start <= end
- Implement `validate_ip()` - checks IP format (use simple check)
- Test with valid and invalid configs

**DONE =**
- Both validation functions return `Result<(), ScanError>`
- They return appropriate errors for invalid input
- You tested both passing and failing cases

**BREAK after this**

---

#### Sub-task 008f: Handle errors in main (15 min)
**Your Task:**
- Change `main()` to return `Result<(), ScanError>`
- Add validation call with `?`
- Observe what happens when error occurs
- Change main signature to use `Box<dyn std::error::Error>` (more flexible)

**DONE =**
- Main returns Result
- Errors are propagated correctly
- You understand `main()` can return Result
- You've seen `Box<dyn Error>` (we'll learn more later)

**BREAK after this** (5 minutes - Sprint 1 complete!)

**Reflection Question:** How does Result-based error handling compare to try/catch in TypeScript? What are the advantages?

**Sprint 1 Complete!** You now understand:
- Variables and mutability
- Functions and return types
- Structs and methods
- Enums and pattern matching
- Option and Result types
- Basic error handling

---

## SPRINT 2: Ownership & Borrowing (THE CRITICAL CONCEPTS)

**Sprint Metadata:**
- Total sub-tasks: 18
- Sequential time: ~5 hours (with breaks)
- Could complete in: 2-3 hyperfocus sessions OR spread across 4-6 days
- **NOTE:** This is the hardest sprint - be patient with yourself!

---

### TASK-009: Understanding Ownership Rules

**Total Time:** ~90 minutes (6 sub-tasks × 15 min)

#### Sub-task 009a: Create and print a vector (15 min)
**Your Task:**
- Create: `let results = vec![ScanResult { port: 80, state: PortState::Open }];`
- Add 2 more results to it
- Print the vector using Debug: `println!("{:?}", results);`
- This will fail - add `#[derive(Debug)]` to your structs/enums

**DONE =**
- Vector created with 3 results
- Code compiles after adding Debug derive
- Prints the vector

**BREAK after this**

---

#### Sub-task 009b: Pass vector to function - observe move (15 min)
**Your Task:**
- Create function: `fn print_results(results: Vec<ScanResult>) { ... }`
- Call it: `print_results(results);`
- Try to use `results` again after the call
- READ the compiler error - don't fix yet

**DONE =**
- Compiler error: "value borrowed here after move" or "use of moved value"
- You can quote the exact error message
- You understand the vector was MOVED into the function

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "What does 'move' mean? Where did the vector go?"

---

#### Sub-task 009c: Understand ownership transfer (15 min)
**Your Task:**
- Draw a diagram (on paper or text) showing:
  1. `results` created → ownership is in main
  2. `print_results(results)` called → ownership moves to function
  3. Function ends → vector is dropped (memory freed)
  4. main tries to use → ERROR, no longer owns it
- Write 3-4 sentences explaining this

**DONE =**
- You have a diagram or written explanation
- You understand each value has ONE owner
- You understand ownership transfers on move
- You know moved values are dropped when owner's scope ends

**BREAK after this**

---

#### Sub-task 009d: Fix by borrowing instead (15 min)
**Your Task:**
- Change function signature: `fn print_results(results: &Vec<ScanResult>)`
- Call with: `print_results(&results);`
- Use `results` again after the call
- Observe it works now!

**DONE =**
- Code compiles
- You can use vector multiple times
- You understand `&` means "borrow, don't take ownership"

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why does & fix this? What's different about borrowing vs moving?"

---

#### Sub-task 009e: Understand Copy vs Move types (15 min)
**Your Task:**
- Experiment with a `u16` variable:
  ```rust
  let port = 80;
  let port2 = port;
  println!("{}", port); // This works!
  ```
- Understand `u16` implements Copy trait
- Try same with `String` - observe it moves instead
- Research: What types are Copy?

**DONE =**
- You understand Copy types are duplicated, not moved
- You know primitives (u16, i32, bool) are Copy
- You know String, Vec are NOT Copy (they're on heap)
- You can explain the difference

**BREAK after this**

---

#### Sub-task 009f: Experiment with ownership transfer (15 min)
**Your Task:**
- Create a function that takes ownership: `fn consume_results(results: Vec<ScanResult>)`
- Inside, it doesn't return anything
- Call it with your vector
- Try to use vector after - observe error
- Understand this pattern: "consuming" a value

**DONE =**
- Function takes ownership and drops value
- You understand when you'd want this (vs borrowing)
- You can explain "consuming" a value

**BREAK after this** (5 minutes)

**Reflection Question:** Compare to Ruby/TypeScript - why doesn't Rust just copy everything? Why have move semantics?

---

### TASK-010: References and Borrowing

**Total Time:** ~90 minutes (6 sub-tasks × 15 min)

#### Sub-task 010a: Multiple immutable borrows (15 min)
**Your Task:**
- Create a ScanConfig
- Create 3 functions that take `&ScanConfig`
- Call all three with the same config
- Observe it works fine

**DONE =**
- Three functions borrow config
- All three calls succeed
- You understand you can have many `&T` borrows

**BREAK after this**

---

#### Sub-task 010b: Try multiple mutable borrows - observe error (15 min)
**Your Task:**
- Create function: `fn update_timeout(config: &mut ScanConfig, timeout: u64)`
- Try to create TWO mutable borrows at once:
  ```rust
  let borrow1 = &mut config;
  let borrow2 = &mut config;
  ```
- READ the compiler error - don't fix yet

**DONE =**
- Compiler error about multiple mutable borrows
- You can quote the error
- You haven't fixed it yet - just observed

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why would Rust prevent two mutable borrows? What could go wrong?"

---

#### Sub-task 010c: Fix with scopes (15 min)
**Your Task:**
- Fix the error using scopes:
  ```rust
  {
      let borrow1 = &mut config;
      // use borrow1
  } // borrow1 ends here

  let borrow2 = &mut config; // Now this works
  ```
- Understand scope controls borrow lifetime

**DONE =**
- Code compiles
- You understand borrows end when scope ends
- You know how to fix "multiple mutable borrow" errors

**BREAK after this**

---

#### Sub-task 010d: Mix immutable and mutable - observe error (15 min)
**Your Task:**
- Try this:
  ```rust
  let read_borrow = &config;
  let write_borrow = &mut config;
  println!("{:?}", read_borrow);
  ```
- Observe error about mixing & and &mut
- Don't fix - just understand why

**DONE =**
- Compiler error about mixing borrows
- You understand: can't have & and &mut at same time
- You know this prevents reading while writing

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why can't you have & and &mut at the same time? What's the data race scenario?"

---

#### Sub-task 010e: The borrowing rules (15 min)
**Your Task:**
- Write down the three borrowing rules:
  1. At any time, you can have EITHER...
  2. ...
  3. ...
- Create examples that violate each rule
- Observe compiler errors

**DONE =**
- You've written all three rules correctly
- You have code examples for each violation
- You understand WHY these rules exist (prevent data races)

**BREAK after this**

---

#### Sub-task 010f: Apply to ScanConfig methods (15 min)
**Your Task:**
- Review your `impl ScanConfig` block
- Identify which methods should use `&self` vs `&mut self`
- Change any that need changing
- Test that borrows work correctly

**DONE =**
- Read-only methods use `&self`
- Mutating methods use `&mut self`
- You can explain the choice for each method

**BREAK after this** (5 minutes)

**Reflection Question:** How do ownership and borrowing prevent data races at compile time? Why is this better than runtime checks?

---

### TASK-011: String vs &str Deep Dive

**Total Time:** ~90 minutes (6 sub-tasks × 15 min)

#### Sub-task 011a: Understand String is owned (15 min)
**Your Task:**
- Create: `let ip = String::from("192.168.1.1");`
- Pass to function that takes ownership: `fn process_ip(ip: String)`
- Try to use `ip` after - observe move
- Understand String is heap-allocated and owned

**DONE =**
- String created and moved
- You get "moved value" error
- You understand String owns its data

**BREAK after this**

---

#### Sub-task 011b: Understand &str is borrowed (15 min)
**Your Task:**
- Create function: `fn print_ip(ip: &str)`
- Call with: `print_ip(&ip)` (borrow the String as &str)
- Call with: `print_ip("127.0.0.1")` (string literal)
- Observe both work

**DONE =**
- Function accepts both &String and string literals
- You understand &str is a "string slice" (borrowed view)
- String literals are &str type

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why can you pass both &String and &str to a function expecting &str?"

---

#### Sub-task 011c: String methods and conversions (15 min)
**Your Task:**
- Experiment with:
  - `"literal".to_string()` → String
  - `my_string.as_str()` → &str
  - `&my_string` → also &str (coercion)
- Create examples of each conversion

**DONE =**
- You can convert between String and &str
- You understand when each conversion happens
- You know `&String` coerces to `&str`

**BREAK after this**

---

#### Sub-task 011d: When to use each type (15 min)
**Your Task:**
- Update `ScanConfig` struct:
  - Should `target_ip` be `String` or `&str`? (hint: ownership)
- Update function parameters:
  - Should they take `String` or `&str`? (hint: borrowing)
- Write guidelines for yourself: "Use String when... Use &str when..."

**DONE =**
- `ScanConfig.target_ip` is `String` (struct owns it)
- Functions take `&str` (they just borrow)
- You have written guidelines

**BREAK after this**

**Socratic Checkpoint:** I'll ask: "Why store String in struct but accept &str in functions?"

---

#### Sub-task 011e: Slicing strings (15 min)
**Your Task:**
- Create: `let ip = String::from("192.168.1.1");`
- Extract first octet: `let first = &ip[0..3];` (type is &str)
- Understand slicing creates &str views
- Experiment with different ranges

**DONE =**
- You can slice strings
- You understand result is &str
- You know about range syntax (0..3, 0..=3, .., etc.)

**BREAK after this**

---

#### Sub-task 011f: Common String pitfalls (15 min)
**Your Task:**
- Try to index: `let c = ip[0];` (will fail!)
- Understand why (strings are UTF-8, not byte-indexed)
- Use: `ip.chars().nth(0)` instead
- Research: Why can't you index strings in Rust?

**DONE =**
- You understand string indexing fails
- You know strings are UTF-8 (char != byte)
- You can iterate with `.chars()` or `.bytes()`

**BREAK after this** (5 minutes - Sprint 2 complete!)

**Reflection Question:** How does String/&str compare to Ruby (mutable strings) or TypeScript (immutable strings)?

**Sprint 2 Complete!** You now understand:
- Ownership rules (the hardest concept!)
- Move vs Copy semantics
- Borrowing rules (& and &mut)
- String vs &str (owned vs borrowed)
- Why Rust is memory safe without GC

**CRITICAL CHECKPOINT:** Before moving to Sprint 3, make sure you can explain:
1. The three ownership rules
2. When a value moves vs copies
3. The borrowing rules (one &mut XOR many &)
4. When to use String vs &str

If any of these are unclear, go back and review. These concepts are FUNDAMENTAL to everything else in Rust.

---

## SPRINT 3: Collections & Iteration

**Sprint Metadata:**
- Total sub-tasks: TBD (will break down as we reach this sprint)
- Estimated time: ~3 hours
- **NOTE:** We'll detail these tasks when you complete Sprint 2

### TASK-012: Vec<T> for Storing Results
_To be broken into 15-min sub-tasks when you reach this sprint_

### TASK-013: HashMap for Port Services
_To be broken into 15-min sub-tasks when you reach this sprint_

---

## SPRINT 4+: Advanced Topics

We'll break down these sprints into 15-minute sub-tasks as you progress. The pattern will be the same:
- Each concept split into small, achievable chunks
- Clear DONE criteria
- Mandatory breaks
- Socratic checkpoints
- Reflection questions

**Upcoming Sprints:**
- Sprint 4: Basic TCP Scanning
- Sprint 5: Async & Concurrency
- Sprint 6: Service Detection
- Sprint 7: CLI & Output
- Sprint 8: Polish & Testing

---

## Task Status Legend

Mark sub-tasks as you complete them:

- **TODO**: Not started
- **IN PROGRESS**: Currently working on (only ONE sub-task at a time!)
- **STUCK**: Been working 30+ min, need Socratic guidance
- **DONE**: Completed and understood

Mark full tasks as DONE when all sub-tasks complete.

---

## Energy Tracking

At the start of each session, record:

**Date:** ___________
**Energy Level:** High / Medium / Low
**Sub-tasks completed:** ___________
**Notes:** ___________

This helps you understand your patterns and plan sessions.

---

## Notes & Insights

### Key "Aha!" Moments
_(Record your insights as you learn)_

-

### Challenges & Solutions
_(Track what was hard and how you overcame it)_

-

### Questions for Later
_(Park questions that come up)_

-

---

## Remember

- **15 minutes** means focused time on ONE thing
- **BREAK after this** is not optional - take it!
- **DONE = criteria** must be met before moving on
- **Stuck protocol**: 30 min → ask for Socratic help → 30 more min → move on if still stuck
- **I guide with questions**, not answers - this builds understanding
- **Your neurodivergence is a strength** - we're working WITH it, not against it

You're not just learning Rust syntax - you're building a mental model of systems programming. This takes time. Be patient with yourself.

Let's build rscout and learn Rust deeply! 🦀
