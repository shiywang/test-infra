package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "model_test.go",
        "mysql_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
)

go_library(
    name = "go_default_library",
    srcs = [
        "model.go",
        "mysql.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//vendor:github.com/jinzhu/gorm",
        "//vendor:github.com/spf13/cobra",
    ],
)

filegroup(
    name = "configs",
    srcs = [],
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
        "//velodrome/sql/testing:all-srcs",
    ],
    tags = ["automanaged"],
)
