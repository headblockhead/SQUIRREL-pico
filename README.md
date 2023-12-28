# SQIREL-Pico
(squirrel)

Simple QMK Inspired Runtime Editable Library (implemented for Pico).

This is an implementation of the SQIREL for the Raspberry Pi Pico.

## Tasks

### Build
Directory: ./build

Builds the keyboard firmware.

```bash
cmake -DCMAKE_BUILD_TYPE=Release ..
make -j4 SQUIRREL-pico
```

### Build-debug
Directory: ./build

Builds the keyboard firmware with debug build type.

```bash
cmake -DCMAKE_BUILD_TYPE=Debug .. 
make -j4 SQUIRREL-pico
cp compile_commands.json ../ # Copies the autocomplete information for ccls.
```

### Clean
Cleans the build directory for a fresh build.

```bash
rm -rf ./build
mkdir build
```

### Init-submodules

Fetches SQUIRREL and the pico-sdk submodules for use in the project.
```bash
git submodule update --init --recursive
```

### Update-submodules
Requires: init-submodules

This fetches the latest version of SQUIRREL and the pico-sdk from their remotes. Be careful of breaking changes!

```bash
git submodule update --remote
```
