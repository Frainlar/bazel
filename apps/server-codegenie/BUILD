load("@rules_python//python:defs.bzl", "py_binary")

py_binary(
    name = "server_codegenie",
    srcs = glob(["**/*.py"]),
    deps = ["@pip//:requirements"],
    main = "app/main.py",  # Update with your FastAPI app entry point
)
