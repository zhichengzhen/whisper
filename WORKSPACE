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

