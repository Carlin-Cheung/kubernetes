load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "common.go",
        "common_unix.go",
        "common_windows.go",
        "names.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/github.com/docker/docker/api",
    importpath = "github.com/docker/docker/api",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/docker/docker/pkg/ioutils:go_default_library",
        "//vendor/github.com/docker/docker/pkg/system:go_default_library",
        "//vendor/github.com/docker/libtrust:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//vendor/github.com/docker/docker/api/types:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
