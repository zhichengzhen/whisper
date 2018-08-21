workspace(name = "com_github_karlstone_whisper")

API_LEVEL = 27
BUILD_TOOLS_VERSION = "27.0.1"

android_sdk_repository(
    name = "androidsdk",
    api_level = API_LEVEL,
    build_tools_version = BUILD_TOOLS_VERSION,
)

local_repository(
    name = "com_github_karlstone_whisper_android",
    path = "android",
)

load("@com_github_karlstone_whisper_android//bazel:gen_deps.bzl", "gen_android_deps")
gen_android_deps(BUILD_TOOLS_VERSION)

local_repository(
    name = "com_github_karlstone_whisper_ios",
    path = "ios"
)

load("@com_github_karlstone_whisper_ios//bazel:gen_deps.bzl", "gen_ios_deps")
gen_ios_deps()

load(
    "@build_bazel_rules_apple//apple:repositories.bzl",
    "apple_rules_dependencies",
)
apple_rules_dependencies()

