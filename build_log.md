# Build Log

## 2026-03-26
### Environment setup
- Installed WSL and Ubuntu on Windows
- Created Linux user account
- Installed required packages:
  - git
  - cmake
  - gcc-arm-none-eabi
  - libnewlib-arm-none-eabi
  - build-essential

### Repository setup
- Cloned `starter-robot-firmware`
- Initialized submodules with:
  - `git submodule update --init --recursive`

### Build issues encountered
- Package download timeout during installation of large ARM-related package
- Missing C++ compiler during CMake build
- Resolved by installing `build-essential`

### Build result
- Successfully built firmware in the `build` directory
- Generated:
  - `main_app.elf`
  - `main_app.uf2`

### Current status
- Software build environment is ready
- Firmware has been compiled successfully
- Waiting for Raspberry Pi Pico W hardware for flashing and testing
