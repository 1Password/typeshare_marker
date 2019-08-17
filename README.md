# typeshare_marker

[Typeshare](https://crates.io/crates/typeshare) is a utility that parses Rust structs and enums and generates code in TypeScript, Swift, and Java for FFI interop.

The `typeshare_marker` implements an attribute for marking Rust types that should be processed by the `typeshare`.

For example:

```toml
# Cargo.toml 

[dependencies]
typeshare_marker = "0.0.1"
```

```rust
// Contents of the src/person.rs file.

#[typeshare]
pub struct Person {
    name: String,
    email: String,
}
```

```bash
$ cargo install typeshare
$ typeshare --type=ts src/person.rs

//
// Generated
//

export interface Person {
	name: string;
	email: string;
}
```

