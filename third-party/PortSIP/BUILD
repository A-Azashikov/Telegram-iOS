load(
  "@build_bazel_rules_apple//apple:apple.bzl",
  "apple_static_framework_import",
)

load("@build_bazel_rules_swift//swift:swift.bzl",
  "swift_library",
)

apple_static_framework_import(
  name = "PortSIPVoIPSDK",
  framework_imports = glob([
    "Frameworks/PortSIPVoIPSDK.framework/**",
  ]),
  sdk_dylibs = [
    "libc++",
    "libresolv",
  ],
  sdk_frameworks = [
    "VideoToolbox",
    "GLKit",
    "MetalKit",
  ],
)

swift_library(
  name = "PortSIPSDKLib",
  module_name = "PortSIPSDKLib",
  srcs = glob([
    "Sources/**/*.swift",
  ]),
  linkopts = [
    "-ObjC",
  ],
  deps = [
    ":PortSIPVoIPSDK",
  ],
  visibility = ["//visibility:public"],
)
