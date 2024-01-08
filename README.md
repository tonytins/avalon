# Avalon

Avalon is a simple proof of concept to how easy it would be to bring .NET Blazor's components to Vue in order to test a theory that the two share a similar Model-View-Controller design compared to React or Solid. Spoilers: they do. Coming from a Blazor background, I accidentally jumped head first into React when transitioning a few Rust projects into desktop applications, and only realized my mistake afterward. Avalon was intended to correct that mistake. xD

It doesn't include Tauri's default hello world example on the front end (thoguh the code is still there on the Rust side) because I wanted to see just how much of the home page's components I could port over, as I'm not that familiar with Vue yet.

## Requirements

### Supported Platforms

| Platform | Versions                           |
| -------- | ---------------------------------- |
| Windows  | 7 or later                         |
| macOS    | 10.15 or later                     |
| Linux    | webkit2gtk 4.1 (e.g. Ubuntu 20.04) |

### Prerequisites

- [Rust](https://www.rust-lang.org/tools/install) 2021 edition
  - [Tauri](https://marketplace.visualstudio.com/items?itemName=tauri-apps.tauri-vscode)
- [VS Code](https://code.visualstudio.com/)
  - [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)

## Getting Started

```shell
$ yarn
$ yarn tauri dev 
```

### Building

```shell
$ yarn tauri build 
```

## License

I hereby waive this project under the public domain - see [UNLICENSE](UNLICENSE) for details.