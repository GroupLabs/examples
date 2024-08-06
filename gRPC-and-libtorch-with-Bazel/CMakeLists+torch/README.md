PyTorch exposes a C++ API that is quite straightforward. In their documentation, they use CMake to add precompiled binaries to the project. See [PyTorch Docs](https://pytorch.org/cppdocs/installing.html) for more information.

# Building
1. Download the appropriate zip archive containing the LibTorch distribution from the [PyTorch website](https://pytorch.org/get-started/locally/). Make sure to select the LibTorch package with C++/Java and unzip the archive before moving forward.

    ```bash
    wget <link/to/libtorch>
    unzip <path/to/libtorch>
    ```

2. Create a build directory and build the application.

    ```bash
    mkdir build
    cd build
    cmake -DCMAKE_PREFIX_PATH=<absolute/path/to/libtorch> ..
    cmake --build . --config Release
    ```

3. Execute the application.

    ```bash
    ./example-app
    ```