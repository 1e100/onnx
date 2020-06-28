workspace(name = "onnx")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("//third_party:cloud_archive.bzl", "minio_archive")

http_archive(
    name = "bazel_skylib",
    sha256 = "9a737999532daca978a158f94e77e9af6a6a169709c0cee274f0a4c3359519bd",
    strip_prefix = "bazel-skylib-1.0.0",
    url = "https://github.com/bazelbuild/bazel-skylib/archive/1.0.0.tar.gz",
)

minio_archive(
    name = "google_benchmark",
    file_path = "minio/deps/src/google-benchmark/v1.5.1.tar.gz",
    sha256 = "23082937d1663a53b90cb5b61df4bcc312f6dee7018da78ba00dd6bd669dfef2",
    strip_prefix = "benchmark-1.5.1",
)

http_archive(
    name = "com_google_protobuf_gh",
    sha256 = "03d2e5ef101aee4c2f6ddcf145d2a04926b9c19e7086944df3842b1b8502b783",
    strip_prefix = "protobuf-3.8.0",
    urls = ["https://github.com/protocolbuffers/protobuf/archive/v3.8.0.tar.gz"],
)

minio_archive(
    name = "com_google_protobuf",
    file_path = "minio/deps/src/protobuf/v3.12.3.tar.gz",
    sha256 = "71030a04aedf9f612d2991c1c552317038c3c5a2b578ac4745267a45e7037c29",
    strip_prefix = "protobuf-3.12.3",
)

load("@com_google_protobuf//:protobuf_deps.bzl", "protobuf_deps")

protobuf_deps()

minio_archive(
    name = "pybind11",
    build_file = "//third_party:pybind11.BUILD",
    file_path = "minio/deps/src/pybind11/v2.5.0.tar.gz",
    sha256 = "97504db65640570f32d3fdf701c25a340c8643037c3b69aec469c10c93dc8504",
    strip_prefix = "pybind11-2.5.0",
)
