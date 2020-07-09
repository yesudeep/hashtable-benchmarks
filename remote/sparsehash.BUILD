load("@rules_cc//cc:defs.bzl", "cc_library")

cc_library(
    name = "sparsehash",
    hdrs = glob([
        "src/google/**/*",
        "src/sparsehash/**/*",
    ]),
    includes = ["src"],
    visibility = ["//visibility:public"],
    deps = [
        "@hashtable_benchmarks//:sparsehash_config",
    ],
)
