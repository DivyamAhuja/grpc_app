load("@com_github_grpc_grpc//bazel:grpc_build_system.bzl", "grpc_proto_library")

package(default_visibility = ["//visibility:public"])

grpc_proto_library(
    name = "greeter_proto",
    srcs = ["src/proto/greeter.proto"]
)

cc_binary(
    name = "server",
    srcs = ["src/server.cc"],
    deps = [
        ":greeter_proto",
        "@com_github_grpc_grpc//:grpc++",
        "@com_github_grpc_grpc//:grpc++_reflection"
    ]
)

cc_binary(
    name = "client",
    srcs = ["src/client.cc"],
    deps = [
        ":greeter_proto",
        "@com_github_grpc_grpc//:grpc++"
    ]
)