package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "join.go",
        "kubefed.go",
        "unjoin.go",
    ],
    importpath = "k8s.io/kubernetes/federation/pkg/kubefed",
    deps = [
        "//federation/apis/federation:go_default_library",
        "//federation/apis/federation/v1beta1:go_default_library",
        "//federation/pkg/kubefed/init:go_default_library",
        "//federation/pkg/kubefed/util:go_default_library",
        "//pkg/api:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/apis/rbac:go_default_library",
        "//pkg/client/clientset_generated/internalclientset:go_default_library",
        "//pkg/kubectl:go_default_library",
        "//pkg/kubectl/cmd:go_default_library",
        "//pkg/kubectl/cmd/templates:go_default_library",
        "//pkg/kubectl/cmd/util:go_default_library",
        "//pkg/kubectl/resource:go_default_library",
        "//pkg/kubectl/util/i18n:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/spf13/cobra:go_default_library",
        "//vendor/github.com/spf13/pflag:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/storage/names:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/util/flag:go_default_library",
        "//vendor/k8s.io/client-go/tools/clientcmd:go_default_library",
        "//vendor/k8s.io/client-go/tools/clientcmd/api:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "join_test.go",
        "unjoin_test.go",
    ],
    importpath = "k8s.io/kubernetes/federation/pkg/kubefed",
    library = ":go_default_library",
    deps = [
        "//federation/apis/federation:go_default_library",
        "//federation/apis/federation/v1beta1:go_default_library",
        "//federation/pkg/kubefed/testing:go_default_library",
        "//federation/pkg/kubefed/util:go_default_library",
        "//pkg/api:go_default_library",
        "//pkg/api/legacyscheme:go_default_library",
        "//pkg/api/testapi:go_default_library",
        "//pkg/apis/rbac/v1:go_default_library",
        "//pkg/kubectl:go_default_library",
        "//pkg/kubectl/cmd/testing:go_default_library",
        "//pkg/kubectl/cmd/util:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//vendor/k8s.io/api/rbac/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/equality:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/serializer:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/diff:go_default_library",
        "//vendor/k8s.io/client-go/dynamic:go_default_library",
        "//vendor/k8s.io/client-go/rest/fake:go_default_library",
        "//vendor/k8s.io/client-go/tools/clientcmd:go_default_library",
        "//vendor/k8s.io/client-go/tools/clientcmd/api:go_default_library",
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
        "//federation/pkg/kubefed/init:all-srcs",
        "//federation/pkg/kubefed/testing:all-srcs",
        "//federation/pkg/kubefed/util:all-srcs",
    ],
    tags = ["automanaged"],
)
