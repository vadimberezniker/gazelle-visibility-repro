workspace(
    name = "repro",
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive", "http_file")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "f6f5ede97567d1c61d6d5227848bb13f419e4ea195b81ba4ca451f20bcd03d66",
    strip_prefix = "rules_go-4706a513acc1f6e5125b476936060ff71bfb8723",
    urls = [
        # TODO(sluongng): this track the unreleased version v0.43.0 of rules_go.
        # See https://github.com/bazelbuild/rules_go/pull/3722#issuecomment-1787954611 for more information.
        # We should replace this once rules_go v0.43.0 is released.
        "https://github.com/bazelbuild/rules_go/archive/4706a513acc1f6e5125b476936060ff71bfb8723.zip",
    ],
)

http_archive(
    name = "bazel_gazelle",
    sha256 = "29218f8e0cebe583643cbf93cae6f971be8a2484cdcfa1e45057658df8d54002",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/bazel-gazelle/releases/download/v0.32.0/bazel-gazelle-v0.32.0.tar.gz",
        "https://github.com/bazelbuild/bazel-gazelle/releases/download/v0.32.0/bazel-gazelle-v0.32.0.tar.gz",
    ],
)


load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies")
load("@io_bazel_rules_go//go:deps.bzl", "go_register_toolchains", "go_rules_dependencies")

go_rules_dependencies()

go_register_toolchains(version = "1.21.0")

gazelle_dependencies()




