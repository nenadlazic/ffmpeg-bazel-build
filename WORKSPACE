workspace(name = "hello_world_workspace")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_foreign_cc",
    sha256 = "9561b3994232ccb033278ade83c2ce48e763e9cae63452cd8fea457bedd87d05",
    strip_prefix = "rules_foreign_cc-816905a078773405803e86635def78b61d2f782d",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/816905a078773405803e86635def78b61d2f782d.tar.gz",
)

load("@rules_foreign_cc//foreign_cc:repositories.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()

new_git_repository(
    name = "ffmpeg_repo",
    build_file = "@//:external_build_files/ffmpeg.BUILD",
    commit = "c7210207555effd194b60dee424fd5632bb388f4",  # This fetches the latest commit
    remote = "https://git.ffmpeg.org/ffmpeg.git",
)

