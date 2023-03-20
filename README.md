# actions-rs-toolchain
GitHub Actions for installing `rust` toolchain according to the [`rust-toolchain.toml`](https://rust-lang.github.io/rustup/overrides.html#the-toolchain-file).

[![license](https://img.shields.io/github/license/CfirTsabari/actions-rs-toolchain.svg)](https://github.com/CfirTsabari/actions-rs-toolchain/blob/master/LICENSE)
[![release](https://img.shields.io/github/release/CfirTsabari/actions-rs-toolchain.svg)](https://github.com/CfirTsabari/actions-rs-toolchain/releases/latest)


> Inspired by [`dtolnay/rust-toolchain`](https://github.com/dtolnay/rust-toolchain).

This action will extend [`dtolnay/rust-toolchain`](https://github.com/dtolnay/rust-toolchain) action and add support for using the rust-toolchain.toml file.
Profile is not be supported and the minimal profile will always be used.

## Getting started

### Create your workflow
```yaml
name: CI
on: pull_request

jobs:
  ci:
    runs-on: windows-latest
    steps:
      - uses: actions/checkout@v3
      - name: Install Rust
        uses: CfirTsabari/actions-rs-toolchain@v1
      - name: print rustc version
        run: rustc --version
```

## License
[MIT License - CfirTsabari/actions-rs-toolchain](https://github.com/CfirTsabari/actions-rs-toolchain/blob/master/LICENSE)


