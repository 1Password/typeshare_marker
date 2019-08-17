# typeshare_marker

[Typeshare](https://crates.io/crates/typeshare) is a utility that parses Rust structs and enums and generates code in TypeScript, Swift, and Java for FFI interop.

The `typeshare_marker` implements an attribute for marking Rust types that should be processed by the `typeshare`.

For example,

```rust
// Contents of src/person.rs file.
#[typeshare]
pub struct Person {
    name: String,
    email: String,
}
```

```bash
cargo install typeshare
typeshare --type=ts src/person.rs
```

