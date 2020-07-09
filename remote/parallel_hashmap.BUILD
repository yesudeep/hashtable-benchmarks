load("@rules_cc//cc:defs.bzl", "cc_library")

licenses(["notice"])

exports_files(["LICENSE"])  # Apache License 2.0

cc_library(
    name = "parallel_hashmap",
    hdrs = [
        "parallel_hashmap/btree.h",
        "parallel_hashmap/meminfo.h",
        "parallel_hashmap/phmap.h",
        "parallel_hashmap/phmap_base.h",
        "parallel_hashmap/phmap_bits.h",
        "parallel_hashmap/phmap_config.h",
        "parallel_hashmap/phmap_dump.h",
        "parallel_hashmap/phmap_fwd_decl.h",
        "parallel_hashmap/phmap_utils.h",
    ],
    includes = ["."],
    visibility = ["//visibility:public"],
)
