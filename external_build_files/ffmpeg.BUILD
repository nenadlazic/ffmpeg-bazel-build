package(default_visibility = ["//visibility:public"])

load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

filegroup(
    name = "ffmpeg_sources",
    srcs = glob(["@ffmpeg_repo/**/*.h", "@ffmpeg_repo/**/*.c", "@ffmpeg_repo/**/*.cpp"]),
    visibility = ["//visibility:public"],
)

filegroup(
    name = "ffmpeg_configure",
    srcs = glob(["@ffmpeg_repo/configure"]),
    visibility = ["//visibility:public"],
)

configure_make(
    name = "ffmpeg_build",
    configure_command = "external/ffmpeg_repo/configure",  # Use the configure script from ffmpeg_repo
    lib_source = ":ffmpeg_sources",  # Reference the filegroup label
    visibility = ["//visibility:public"],
    configure_options = [
        "--enable-shared",
        "--disable-static",
        "--disable-programs",
        "--enable-swscale",
        "--enable-debug=3",
    ],
    out_headers_only = True,
)

