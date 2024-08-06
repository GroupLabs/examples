This directory gives an example of how to use Bazel to add libtorch as a dependency.

# Building
1. Download the appropriate zip archive containing the LibTorch distribution from the [PyTorch website](https://pytorch.org/get-started/locally/). Make sure to select the LibTorch package with C++/Java and unzip the archive before moving forward.
    ```bash
    wget <link/to/libtorch>
    unzip <path/to/libtorch>
    ```

2. Create an external directory, and move the libtorch directory to it.
    ```bash
    mkdir external
    mv <path/to/libtorch> <path/to/external/directory>
    ```

    It should now look something like this:
    ```bash
    .
    ├── BUILD
    ├── README.md
    ├── WORKSPACE
    ├── external
    │   └── libtorch
    ├── libtorch.BUILD
    └── main.cc
    ```

3. Build and run the example.
    ```bash
    bazel run --enable_bzlmod=false //:main
    ```

4. (Optional) Use the alternate `WORKSPACE` file. With this option, you can skip downloading libtorch, and have Bazel handle it for you. Thereofore, if you choose to use the alternative `WORKSPACE` file, you can skip steps 1 and 2, and directly run with bazel. Don't forget to update the link to the desired zip archive.

    a. Select the `WORKSPACE` file.
    ```bash
    mv WORKSPACE notWORKSPACE
    mv altWORKSPACE WORKSPACE
    ```

    b. Build and run the example.
    ```bash
    bazel run --enable_bzlmod=false //:main
    ```
