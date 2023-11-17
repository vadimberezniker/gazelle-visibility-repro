load("@bazel_gazelle//:def.bzl", "gazelle", "gazelle_binary")

gazelle_binary(
    name = "gazelle_binary",
    languages = [
        "@bazel_gazelle//language/go",
        "@bazel_gazelle//language/bazel/visibility:go_default_library",
    ],
)

# gazelle:prefix github.com/vadimberezniker/repro
# gazelle:build_file_name BUILD,BUILD.bazel
gazelle(
    name = "gazelle",
    gazelle = ":gazelle_binary",
)
