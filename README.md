vcpkg-freeze
===

This tool creates a file system registry for the currently installed vcpkg packages (in manifest mode only).

The idea here is to avoid having all of vcpkg installed as a git submodule.

Usage
---

In a project managed with a vcpkg manifest:

```bash
vcpkg install --x-feature=feature1 --x-feature=...
vcpkg-freeze
```

Its important to note that if your project has optional features you should specify all features to `vcpkg install` with `--x-feature` flags so that all required ports are frozen.
