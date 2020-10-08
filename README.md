# *Transparent* Visual Studio Code - Open Source ("Code - OSS")
[![Build Status](https://dev.azure.com/vscode/VSCode/_apis/build/status/VS%20Code?branchName=master)](https://aka.ms/vscode-builds)
[![Feature Requests](https://img.shields.io/github/issues/microsoft/vscode/feature-request.svg)](https://github.com/microsoft/vscode/issues?q=is%3Aopen+is%3Aissue+label%3Afeature-request+sort%3Areactions-%2B1-desc)
[![Bugs](https://img.shields.io/github/issues/microsoft/vscode/bug.svg)](https://github.com/microsoft/vscode/issues?utf8=✓&q=is%3Aissue+is%3Aopen+label%3Abug)
[![Gitter](https://img.shields.io/badge/chat-on%20gitter-yellow.svg)](https://gitter.im/Microsoft/vscode)

The goal of this fork is to make a version of vscode that can have fully working window transparency and nice effects to go with that.

## Building And Running
[If the instructions below fail](https://github.com/Microsoft/vscode/wiki/How-to-Contribute#build-and-run)

### Build
1. navigate to the project `cd vscode`
2. install dependencies with `yarn`
3. build project: `yarn watch`

### Running
- Linux / macOS: `./scripts/code.sh --enable-transparent-visuals`
- Windows: `.\scripts\code.bat --enable-transparent-visuals`

## Packaging
vscode can be packaged for: `win32-ia32 | win32-x64 | darwin | linux-ia32 | linux-x64 | linux-arm`
- `gulp` is used to package
  - `vscode-[platform]`: Builds a packaged version for [platform]
  - `vscode-[platform]-min`: Builds a packaged and minified version for [platform]
    - Note: may need to add `--max-old-space-size=6500` to limit the memory used in packaging, my computer crashed a few times trying to package without that flag

Many of the core components and extensions to VS Code live in their own repositories on GitHub. For example, the [node debug adapter](https://github.com/microsoft/vscode-node-debug) and the [mono debug adapter](https://github.com/microsoft/vscode-mono-debug) have their own repositories. For a complete list, please visit the [Related Projects](https://github.com/microsoft/vscode/wiki/Related-Projects) page on our [wiki](https://github.com/microsoft/vscode/wiki).

Example: Packaging for Arch Linux:
- `vscode-linux-x64-min`

VS Code includes a set of built-in extensions located in the [extensions](extensions) folder, including grammars and snippets for many languages. Extensions that provide rich language support (code completion, Go to Definition) for a language have the suffix `language-features`. For example, the `json` extension provides coloring for `JSON` and the `json-language-features` provides rich language support for `JSON`.

## Development Container

This repository includes a Visual Studio Code Remote - Containers / Codespaces development container.

- For [Remote - Containers](https://aka.ms/vscode-remote/download/containers), use the **Remote-Containers: Open Repository in Container...** command which creates a Docker volume for better disk I/O on macOS and Windows.
- For Codespaces, install the [Visual Studio Codespaces](https://aka.ms/vscs-ext-vscode) extension in VS Code, and use the **Codespaces: Create New Codespace** command.

Docker / the Codespace should have at least **4 Cores and 6 GB of RAM (8 GB recommended)** to run full build. See the [development container README](.devcontainer/README.md) for more information.

## Current Transparent Themes
- dark vs, dark plus
- monokai

![](screenshot1.png)
![](screenshot2.png)

## License

Copyright (c) Microsoft Corporation. All rights reserved.

Licensed under the [MIT](LICENSE.txt) license.
