load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "generated_expansion.go",
        "appgroup.go",
        "appgroup_client.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/github.com/diktyo-io/appgroup-api/pkg/generated/clientset/versioned/typed/appgroup/v1alpha1",
    importpath = "github.com/diktyo-io/appgroup-api/pkg/generated/clientset/versioned/typed/appgroup/v1alpha1",
    visibility = ["//visibility:public"],
    deps = [
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//staging/src/k8s.io/client-go/rest:go_default_library",
        "//github.com/diktyo-io/appgroup-api/pkg/apis/appgroup/v1alpha1:go_default_library",
        "//github.com/diktyo-io/appgroup-api/pkg/generated/clientset/versioned/scheme:go_default_library",
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
        "//github.com/diktyo-io/appgroup-api/pkg/generated/clientset/versioned/typed/appgroup/v1alpha1/fake:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
