load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["factory_interfaces.go"],
    importmap = "k8s.io/kubernetes/vendor/github.com/diktyo-io/appgroup-api/pkg/generated/informers/externalversions/internalinterfaces",
    importpath = "github.com/diktyo-io/appgroup-api/pkg/generated/informers/externalversions/internalinterfaces",
    visibility = ["//visibility:public"],
    deps = [
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/client-go/tools/cache:go_default_library",
        "//github.com/diktyo-io/appgroup-api/pkg/generated/clientset/versioned:go_default_library",
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
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
