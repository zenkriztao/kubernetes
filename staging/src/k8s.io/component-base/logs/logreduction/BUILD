load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["logreduction.go"],
    importmap = "k8s.io/kubernetes/vendor/k8s.io/component-base/logs/logreduction",
    importpath = "k8s.io/component-base/logs/logreduction",
    visibility = ["//visibility:public"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["logreduction_test.go"],
    embed = [":go_default_library"],
)
