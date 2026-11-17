# OSB Toolkit

A minimal GUI toolkit for OSB (Operating System Basic) freestanding programs.

## Overview

`osb.toolkit` provides a small, text-mode GUI framework for building interactive applications on the OSB platform. It includes window management, controls, graphics primitives, and desktop/input handling — all designed for freestanding NativeAOT environments.

## What's Included

- **App.cs** - Application lifecycle management
- **Control.cs** - Base control class
- **Desktop.cs** - Desktop/window manager
- **Desktop.Input.cs** - Mouse/keyboard input handling
- **Desktop.Paint.cs** - Rendering and repaint logic
- **Graphics.cs** - Drawing primitives
- **Paint.cs** - Paint operations
- **Types.cs** - Common types and structures
- **Window.cs** - Window management

## Usage

Other OSB projects (like osb.xwin) reference this toolkit to build GUI applications. The toolkit is designed to work with the freestanding runtime constraints of the OSB ecosystem.

## Building

```bash
dotnet build
```

## Part of OSB

This is part of the [OSB](https://github.com/osb-foundation) - Operating System Basic project, a DOS-like operating system built from scratch.

## License

MIT License - see [LICENSE](LICENSE) for details.