load(
    "//bazel:pgv_proto_library.bzl",
    "pgv_cc_proto_library",
)

proto_library(
    name = "test_proto",
    srcs = ["test.proto"],
    visibility = ["//visibility:public"],
    deps = [
        "@com_google_protobuf//:any_proto",
    ],
)

pgv_cc_proto_library(
  name = "test_cc_proto",
  deps = [":test_proto"],
  visibility = ["//visibility:public"],
)


cc_binary(
    name = "cc-mfjt-test",
    srcs = ["main.cc"],
    visibility = ["//visibility:public"],
    deps = [
        ":test_cc_proto",
    ],
)
