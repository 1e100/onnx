load("@rules_cc//cc:defs.bzl", "cc_library", "cc_proto_library")
load("@rules_proto//proto:defs.bzl", "proto_library")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "onnx-lib",
    srcs = glob(
        [
            "onnx/*.cc",
            "onnx/common/*.cc",
            "onnx/defs/*.cc",
            "onnx/defs/controlflow/*.cc",
            "onnx/defs/experiments/*.cc",
            "onnx/defs/generator/*.cc",
            "onnx/defs/logical/*.cc",
            "onnx/defs/math/*.cc",
            "onnx/defs/nn/*.cc",
            "onnx/defs/object_detection/*.cc",
            "onnx/defs/quantization/*.cc",
            "onnx/defs/reduction/*.cc",
            "onnx/defs/rnn/*.cc",
            "onnx/defs/sequence/*.cc",
            "onnx/defs/tensor/*.cc",
            "onnx/defs/traditionalml/*.cc",
            "onnx/optimizer/*.cc",
            "onnx/shape_inference/*.cc",
            "onnx/version_converter/*.cc",
        ],
        exclude = [
            "onnx/cpp2py_export.cc",
        ],
    ) + [
        "onnx/defs/training/defs.cc",
    ],
    hdrs = glob([
        "onnx/*.h",
        "onnx/version_converter/*.h",
        "onnx/common/*.h",
        "onnx/defs/*.h",
        "onnx/defs/tensor/*.h",
        "onnx/shape_inference/*.h",
        "onnx/optimizer/*.h",
        "onnx/optimizer/passes/*.h",
        "onnx/version_converter/adapters/*.h",
    ]),
    defines = [
        "ONNX_ML=1",
        "ONNX_NAMESPACE=onnx",
        "ONNX_USE_LITE_PROTO=onnx",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":proto-ml-lib",
    ],
)

proto_library(
    name = "onnx-ml-proto",
    srcs = [
        "onnx/onnx-ml.proto",
        "onnx/onnx-operators-ml.proto",
    ],
)

cc_proto_library(
    name = "proto-ml-lib",
    deps = [":onnx-ml-proto"],
)
