# Nexus++ Language Documentation

![Nexus++ Banner](https://nexuspp.dev/assets/banner.png)

## Table of Contents
- [Installation](#installation)
- [IDE Setup](#ide-setup)
- [Language Basics](#language-basics)
- [Standard Library](#standard-library)
- [Advanced Features](#advanced-features)
- [Examples](#examples)
- [Community](#community)

---

## Installation

### System Requirements
- x86_64 or ARM64 processor
- 4GB RAM minimum
- 2GB disk space

### Download Links
| Platform | Installer | Checksum |
|----------|----------|----------|
| Windows | [nexuspp-1.0-x64.exe](https://dl.nexuspp.dev/win) | `sha256: a1b2...` |
| macOS | [nexuspp-1.0.dmg](https://dl.nexuspp.dev/mac) | `sha256: c3d4...` |
| Linux | [nexuspp-1.0.deb](https://dl.nexuspp.dev/linux) | `sha256: e5f6...` |

### Build from Source
```bash
git clone https://github.com/nexuspp/compiler
cd compiler
./configure --optimize=native
make -j8
sudo make install