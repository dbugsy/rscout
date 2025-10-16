# rscout - Network Reconnaissance Scanner

A high-performance network reconnaissance tool built in Rust for CTF competitions and security research.

## Project Vision

Build a practical, fast, and reliable network scanner that you'll actually use in CTFs, while learning Rust's systems programming concepts deeply.

## Core Features (Roadmap)

### Phase 1: Foundation
- Single-target TCP port scanning
- Basic command-line interface
- Simple text output

### Phase 2: Concurrency
- Async/parallel scanning
- Multiple ports simultaneously
- Progress indicators

### Phase 3: Intelligence
- Service detection
- Banner grabbing
- OS fingerprinting hints

### Phase 4: Scaling
- Multiple targets (IP ranges, CIDR)
- Smart rate limiting
- Stealth scanning options

### Phase 5: Reporting
- JSON/CSV/Markdown output
- Scan profiles/templates
- Result filtering

### Phase 6: Web Interface (Optional)
- Real-time scan monitoring
- Historical scan results
- Web-based configuration

## Technical Learning Goals

### Rust Concepts You'll Master

1. **Ownership & Borrowing**
   - Managing network connections and buffers
   - Passing data between async tasks
   - Understanding zero-copy operations

2. **Error Handling**
   - Network errors (timeouts, refused connections)
   - Parse errors (invalid IPs, ports)
   - Graceful degradation

3. **Async/Await & Concurrency**
   - tokio runtime
   - Concurrent TCP connections
   - Channels for task coordination
   - Avoiding race conditions

4. **Memory Efficiency**
   - Buffer management for network I/O
   - Efficient data structures for results
   - Streaming results vs collecting

5. **Low-Level Networking**
   - TCP/IP fundamentals
   - Socket programming
   - Binary protocol handling
   - Timeout and retry logic

## Architecture

```
rscout/
├── src/
│   ├── main.rs           # CLI entry point
│   ├── lib.rs            # Library exports
│   ├── scanner/
│   │   ├── mod.rs        # Scanner orchestration
│   │   ├── tcp.rs        # TCP scanning logic
│   │   └── udp.rs        # UDP scanning (later)
│   ├── detector/
│   │   ├── mod.rs        # Service detection
│   │   └── banners.rs    # Banner grabbing
│   ├── output/
│   │   ├── mod.rs        # Output formatting
│   │   ├── json.rs       # JSON output
│   │   └── text.rs       # Human-readable output
│   └── config/
│       └── mod.rs        # Configuration handling
├── tests/
│   └── integration/      # Integration tests
├── examples/             # Usage examples
└── Cargo.toml           # Dependencies
```

## Development Principles

1. **Test-Driven**: Write tests for each feature
2. **Incremental**: Small, working iterations
3. **Performance-Aware**: Benchmark and optimize
4. **Real-World Ready**: Actually usable in CTFs
5. **Learn by Doing**: Build it yourself with guidance

## Success Criteria

- [ ] Scans ports faster than nmap for common cases
- [ ] Handles errors gracefully (no panics in normal operation)
- [ ] Provides clear, actionable output
- [ ] Can scan full port range (1-65535) efficiently
- [ ] You understand every line of code
- [ ] You can explain ownership, borrowing, and async to others

## Comparison to Existing Tools

**vs nmap**:
- Simpler, focused on speed
- Better for quick CTF reconnaissance
- Less comprehensive, more specialized

**vs masscan**:
- Similar speed goals
- More structured output
- Learning-oriented codebase

**vs rustscan**:
- Similar tech stack
- Our own feature set
- Deeper understanding from building it yourself
