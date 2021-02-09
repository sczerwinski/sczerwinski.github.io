---
title: Wavefront OBJ IntelliJ Plugin
layout: toc-page
abstract: Wavefront OBJ file type and 3D preview plugin for IntelliJ platform
keywords: 3d,wavefront,obj,intellij,plugin
project: wavefront-obj-intellij-plugin
---

{% include breadcrumbs-project.html %}

![Build][build_badge]
[![Version][jb_version_badge]][jb_plugin_page]
[![Downloads][jb_download_badge]][jb_plugin_page]
[![Source][gh_badge]][gh_project]
![License][gh_license_badge]

## Features

### Supported features

- OBJ file format,
- MTL file format,
- navigation between OBJ and MTL files,
- 3D preview of OBJ file:
  - text only, preview only, or split,
  - selection of up axis,
  - Gouraud shading model.

### Planned features

The following features are already under consideration, so please refrain from requesting them in
issue tracker.

- 3D preview improvements:
  - additional shading models: flat and Phong,
  - textures,
  - highlighting selected element,
  - applying materials from MTL files.

## Supported operating systems

3D preview is supported for:
- Windows:
  - i586
  - AMD64
- macOS
- Linux:
  - i586
  - AMD64
  - ARMv6hf
  - AArch64

## Installation

- Using IDE built-in plugin system:

  <kbd>Preferences</kbd> > <kbd>Plugins</kbd> > <kbd>Marketplace</kbd> >
  <kbd>Search for "Wavefront OBJ"</kbd> > <kbd>Install Plugin</kbd>

- Manually:

  Download the
  [latest release][latest_release]
  and install it manually using:

  <kbd>Preferences</kbd> > <kbd>Plugins</kbd> > <kbd>⚙️</kbd> >
  <kbd>Install plugin from disk...</kbd>

## Usage

### OBJ File Type And Editor

After installation, `.obj` and `.mtl` file extension will be automatically
associated with Wavefront OBJ/MTL file format and editor.

#### 3D Preview Controls

- Hold mouse left button on the 3D preview and move to pan the camera.
- Use mouse wheel to zoom in/out.

### Settings

- To change Wavefront OBJ editor color scheme, use:

  <kbd>Preferences</kbd> > <kbd>Editor</kbd> > <kbd>Color Scheme</kbd> > <kbd>Wavefront OBJ</kbd>

- To change Wavefront MTL editor color scheme, use:

  <kbd>Preferences</kbd> > <kbd>Editor</kbd> > <kbd>Color Scheme</kbd> > <kbd>Wavefront MTL</kbd>

- To change plugin configuration, use

  <kbd>Preferences</kbd> > <kbd>Languages & Frameworks</kbd> > <kbd>Wavefront OBJ</kbd>

[build_badge]: https://github.com/sczerwinski/wavefront-obj-intellij-plugin/workflows/Build/badge.svg
[jb_version_badge]: https://img.shields.io/jetbrains/plugin/v/14843-wavefront-obj
[jb_download_badge]: https://img.shields.io/jetbrains/plugin/d/14843-wavefront-obj
[jb_plugin_page]: https://plugins.jetbrains.com/plugin/14843-wavefront-obj
[gh_badge]: https://img.shields.io/badge/source-GitHub-blue.svg
[gh_project]: https://github.com/sczerwinski/wavefront-obj-intellij-plugin
[gh_license_badge]: https://img.shields.io/github/license/sczerwinski/wavefront-obj-intellij-plugin.svg
[wikipedia_obj]: https://en.wikipedia.org/wiki/Wavefront_.obj_file
[latest_release]: https://github.com/sczerwinski/wavefront-obj-intellij-plugin/releases/latest
