# Minimal wxWidgets (CMake + vcpkg toolchain)

A 'Hello, world' for building with CMake, using vcpkg (classic mode) for dependencies.

## Quick, fast, in a hurry

1. Clone the template somewhere, obviously :)
2. Ensure wXwidgets is installed: `vcpkg install wxwidgets`
3. Configure: `cmake -S . -B build`
4. Build: `cmake --build build`