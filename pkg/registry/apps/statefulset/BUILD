package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "registry.go",
        "strategy.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/registry/apps/statefulset",
    deps = [
        "//pkg/api/legacyscheme:go_default_library",
        "//pkg/api/pod:go_default_library",
        "//pkg/apis/apps:go_default_library",
        "//pkg/apis/apps/validation:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/equality:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/internalversion:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/validation/field:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/endpoints/request:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/registry/rest:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/storage/names:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["strategy_test.go"],
    importpath = "k8s.io/kubernetes/pkg/registry/apps/statefulset",
    library = ":go_default_library",
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/apis/apps:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/endpoints/request:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/registry/rest:go_default_library",
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
        "//pkg/registry/apps/statefulset/storage:all-srcs",
    ],
    tags = ["automanaged"],
)
