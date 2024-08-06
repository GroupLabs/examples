cc_library(
    name = "libtorch",
    srcs = glob([
        "lib/libc10.dylib",
        "lib/libfbjni.dylib",
        "lib/libomp.dylib",
        "lib/libpytorch_jni.dylib",
        "lib/libshm.dylib",
        "lib/libtorch.dylib",
        "lib/libtorch_cpu.dylib",
        "lib/libtorch_global_deps.dylib",
        ]),
    hdrs = glob([
        "include/**/*.h",
    ]),
    includes = [
        "include",
        "include/torch/csrc/api/include",
    ],
    strip_include_prefix = "include",
    visibility = ["//visibility:public"],
)