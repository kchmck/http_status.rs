# uhttp\_status -- HTTP status code formatter

[Documentation](https://docs.rs/uhttp_status)

This crate provides an HTTP status code formatter, split out from
[hyper.rs](https://hyper.rs).

## Example

```rust
use uhttp_status::{StatusCode, StatusClass};

assert_eq!(format!("{}", StatusCode::NotFound), "404 Not Found");
assert_eq!(format!("{}", StatusCode::Ok), "200 OK");
assert_eq!(StatusCode::NotImplemented.class(), StatusClass::ServerError);
```

## Usage

This [crate](https://crates.io/crates/uhttp_status) can be used through cargo by
adding it as a dependency in `Cargo.toml`:

```toml
[dependencies]
uhttp_status = "0.10.0"
```
and importing it in the crate root:

```rust
extern crate uhttp_status;
```
