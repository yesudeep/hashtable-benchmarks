load("@rules_cc//cc:defs.bzl", "cc_library")

config_setting(
    name = "platform_linux",
    constraint_values = [
        "@bazel_tools//platforms:linux",
    ],
)

config_setting(
    name = "platform_osx",
    constraint_values = [
        "@bazel_tools//platforms:osx",
    ],
)

cc_library(
    name = "folly",
    srcs = [
        "folly/FileUtil.cpp",
        "folly/ScopeGuard.cpp",
        "folly/container/detail/F14Table.cpp",
        "folly/lang/Assume.cpp",
        "folly/lang/SafeAssert.cpp",
        "folly/net/NetOps.cpp",
        "folly/portability/SysUio.cpp",
    ],
    hdrs = glob([
        "folly/**/*.h",
    ]),
    defines = select({
        ":platform_linux": [
            "FOLLY_NO_CONFIG",
            "FOLLY_HAVE_MEMRCHR",
            "FOLLY_HAVE_SENDMMSG",
            "FOLLY_HAVE_RECVMMSG",
        ],
        ":platform_osx": [
            "FOLLY_NO_CONFIG",
            "FOLLY_HAVE_CLOCK_GETTIME",
            "FOLLY_HAVE_PWRITEV=0",
            "FOLLY_HAVE_PREADV=0",
        ],
    }),
    includes = ["."],
    visibility = ["//visibility:public"],
    deps = [
        "@boost//:preprocessor",
        "@com_github_google_double_conversion//:double-conversion",
        "@com_github_google_glog//:glog",
    ],
)
