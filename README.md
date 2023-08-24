# FFmpeg Bazel Build Scripts

This repository provides Bazel build scripts for building FFmpeg, a powerful multimedia framework used for handling audio, video, and other multimedia streams. FFmpeg uses the traditional "configure-make" pattern (makefiles) as its native build system for generating its libraries and binaries.

## Overview
FFmpeg is a widely used multimedia framework known for its versatility and capabilities in working with various multimedia formats. This repository offers an alternative approach to building FFmpeg using Bazel, a modern build system designed for scalability, extensibility, and cross-platform development.

## Why Bazel?
While FFmpeg traditionally uses makefiles as its native build system, Bazel offers advantages such as faster and more reliable incremental builds, improved dependency management, and the ability to integrate with other build systems and tools. This repository explores the use of Bazel to build FFmpeg, providing an alternative for those interested in harnessing the benefits of both FFmpeg and Bazel.

## Getting Started

To use the Bazel build scripts and build FFmpeg with Bazel, use this command:

`bazel build --spawn_strategy=standalone :ffmpeg_build`
