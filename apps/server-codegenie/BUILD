py_library(
    name = "server_codegenie_lib",
    srcs = glob(["**/*.py"]),
    deps = [
        "@pip_deps//fastapi",
        "@pip_deps//uvicorn",
    ],
)

py_binary(
    name = "server_codegenie",
    srcs = ["app/main.py"],
    deps = [":server_codegenie_lib"],
)
