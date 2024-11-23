load("@rules_nodejs//nodejs:defs.bzl", "nodejs_binary")

nodejs_binary(
    name = "client_codegenie",
    entry_point = "node_modules/.bin/next",
    data = glob(["**"]),
    args = ["build"],
)
