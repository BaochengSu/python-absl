licenses(["notice"])  # New BSD, Python Software Foundation

exports_files(["LICENSE"])

py_library(
    name = "unittest3_backport",
    srcs = ["__init__.py"],
    srcs_version = "PY2AND3",
    visibility = ["//absl/testing:__pkg__"],
    deps = [
        ":case",
        ":result",
    ],
)

py_library(
    name = "case",
    srcs = ["case.py"],
    srcs_version = "PY2AND3",
    deps = [
        "@six_archive//:six",
    ],
)

py_library(
    name = "result",
    srcs = ["result.py"],
    srcs_version = "PY2AND3",
    deps = [
        "@six_archive//:six",
    ],
)

py_test(
    name = "tests/unittest3_backport_test",
    size = "small",
    srcs = ["tests/unittest3_backport_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [
        "//absl/testing:absltest",
        "//absl/testing:xml_reporter",
        "@mock_archive//:mock",
        "@six_archive//:six",
    ],
)
