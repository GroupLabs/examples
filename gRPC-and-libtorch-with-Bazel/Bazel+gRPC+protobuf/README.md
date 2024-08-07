gRPC is well supported by Bazel as it is the build tool of choice for the internal team. However, it can be unclear on how to properly set it up. See the online [support guide](https://grpc.github.io/grpc/core/md_doc_bazel_support.html) and [quickstart](https://grpc.io/docs/languages/cpp/quickstart/).

# Building

1. Build and run the example. This will generate the proto files and start a server that you can interact with.

    ```bash
    bazel run --enable_bzlmod=false //:main
    ```