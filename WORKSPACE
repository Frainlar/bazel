workspace(name = "bazel_monorepo")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Bazel Node.js rules
http_archive(
    name = "rules_nodejs",
    url = "https://github.com/aspect-build/rules_nodejs/releases/download/v1.8.0/rules_nodejs-v1.8.0.tar.gz",
    strip_prefix = "rules_nodejs-v1.8.0",
)

load("@rules_nodejs//node:repositories.bzl", "node_repositories")

node_repositories(
    package_manager = "bun",
    lock_file = "bun.lockb",
)

# Python rules
http_archive(
    name = "rules_python",
    url = "https://github.com/bazelbuild/rules_python/releases/download/0.20.0/rules_python-0.20.0.tar.gz",
    strip_prefix = "rules_python-0.20.0",
)

load("@rules_python//python:pip.bzl", "pip_install")

pip_install(
    name = "pip_deps",
    requirements = "//apps/server-codegenie:requirements.txt",
)
