load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "scheduler_interface.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/scheduler/algorithm",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/scheduler/apis/extender/v1:go_default_library",
        "//pkg/scheduler/nodeinfo:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
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
        "//pkg/scheduler/algorithm/predicates:all-srcs",
        "//pkg/scheduler/algorithm/priorities:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
