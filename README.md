# Camx Metadata

The camx-metadata is a camera metadata management library that provides a structured interface for handling camera-related metadata in embedded systems. CAMX Metadata is a C library that implements a robust metadata packet system for camera applications. It's based on the Android Open Source Project's camera metadata framework.

Core Functionality:
Metadata Packet Management: Allocates, manages, and manipulates camera metadata structures with fixed capacity for entries and data
Entry Operations: Add, retrieve, find, update, and delete metadata entries with type safety
Data Type Support: Handles 6 data types (byte, int32, float, int64, double, rational)
Sorting & Searching: Supports both linear and binary search for efficient metadata lookups
Validation: Comprehensive structure validation to detect corruption or misalignment
Vendor Tags: Extensible vendor-specific tag support for OEM customization

Memory Management:
```
-Contiguous memory layout for efficient serialization and copying
-Proper alignment handling for different data types
-Compact and full-size metadata representations
-Support for in-place metadata placement in pre-allocated buffers
```

Use Cases:
```
-Camera HAL (Hardware Abstraction Layer) implementations
-Camera framework metadata handling
-Capture request/result processing
-Camera characteristics and capabilities reporting
```

## Compilation Instructions

### Download source code

Clone the source code from Github:

```
git clone https://github.com/qualcomm-linux/camx-metadata.git
cd camx-metadata
```

### Build the source code
Run CMake to generate the Makefile and build

```
cmake -B build -S . -DCMAKE_INSTALL_PREFIX=/usr && cmake --build build
```

## Development

Contributions are welcome! Please refer to the [CONTRIBUTING.md](CONTRIBUTING.md) file for full details on how to contribute to this project, including:

- [Branching strategy](CONTRIBUTING.md#branching-strategy)
- [Submitting a pull request](CONTRIBUTING.md#submitting-a-pull-request)

## License

camx-metadata is based on the camera metadata library from the Android Open
Source Project ([platform/system/media](https://android.googlesource.com/platform/system/media)),
and is distributed under the following licenses:

- The code under `camera/` and `private/camera/`, imported from AOSP, is
  licensed under the [Apache License 2.0](https://spdx.org/licenses/Apache-2.0.html).
  See [LICENSES/Apache-2.0.txt](LICENSES/Apache-2.0.txt) for the full license
  text. Files modified from AOSP carry a notice describing the change.
  Where those changes were written by Qualcomm Technologies, Inc., they are
  licensed under the
  [BSD-3-Clause-Clear License](https://spdx.org/licenses/BSD-3-Clause-Clear.html),
  and the file is tagged `SPDX-License-Identifier: Apache-2.0 AND BSD-3-Clause-Clear`.
- The build files written for this project (`CMakeLists.txt` and
  `camx_metadata.pc.in`) are licensed under the
  [BSD-3-Clause-Clear License](https://spdx.org/licenses/BSD-3-Clause-Clear.html).
  See [LICENSE.txt](LICENSE.txt) for the full license text.

Each source file states its license with an `SPDX-License-Identifier` tag.
