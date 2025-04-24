load("@rules_cc//cc:defs.bzl", "objc_library")

package(default_visibility = ["//visibility:public"])

objc_library(
    name = "GULEnvironment",
    srcs = glob([
        "GoogleUtilities/Environment/**/*.m",
    ]),
    hdrs = glob([
        "GoogleUtilities/Environment/Public/**/*.h",
    ]),
    enable_modules = True,
    includes = [
        "GoogleUtilities/Environment/Public",
    ],
    module_name = "GULEnvironment",
    sdk_frameworks = [
        "CoreTelephony",
        "Security",
        "SystemConfiguration",
    ],
    deps = [
        "@google_utilities//third_party/IsAppEncrypted",
    ],
)

objc_library(
    name = "GULLogger",
    srcs = glob([
        "GoogleUtilities/Logger/**/*.m",
    ]),
    hdrs = glob([
        "GoogleUtilities/Logger/Public/**/*.h",
    ]),
    enable_modules = True,
    includes = [
        "GoogleUtilities/Logger/Public",
    ],
    module_name = "GULLogger",
    deps = [
        ":GULEnvironment",
    ],
)

objc_library(
    name = "GULUserDefaults",
    srcs = glob([
        "GoogleUtilities/UserDefaults/**/*.m",
    ]),
    hdrs = glob([
        "GoogleUtilities/UserDefaults/Public/**/*.h",
    ]),
    enable_modules = True,
    includes = [
        "GoogleUtilities/UserDefaults/Public",
    ],
    module_name = "GULUserDefaults",
    deps = [
        ":GULLogger",
    ],
)
