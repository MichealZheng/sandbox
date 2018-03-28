package(default_visibility = ["//visibility:public"])

load("@org_pubref_rules_protobuf//cpp:rules.bzl", "cpp_proto_library")

genrule(
     name = "copy_file",
     srcs = ["simple.proto"],
     outs = ["copy.proto"],
     cmd = "cat $(location simple.proto) > $@",
     message = "copy",
)

cpp_proto_library(
   name = "default_library",
   protos = ["simple.proto"],
)

cpp_proto_library(
   name = "copy_library",
   protos = ["copy.proto"],   
   with_grpc = True,
)

