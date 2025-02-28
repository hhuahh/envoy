# Copyright 2020 The Bazel Authors. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# This file is auto-generated by github.com/bazelbuild/bazel-toolchains/pkg/rbeconfigsgen
# and should not be modified directly.

package(default_visibility = ["//visibility:public"])


toolchain(
    name = "cc-toolchain",
    exec_compatible_with = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
        "@bazel_tools//tools/cpp:clang",
    ],
    target_compatible_with = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
    ],
    toolchain = "//third_party/rbe_configs/cc:cc-compiler-k8",
    toolchain_type = "@bazel_tools//tools/cpp:toolchain_type",
)

platform(
    name = "platform",
    parents = ["@local_config_platform//:host"],
    constraint_values = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
        "@bazel_tools//tools/cpp:clang",
    ],
    exec_properties = {
        # Please update both the commented tag and the sha256
        # b0ff77ae3f25b0bf595f9b8bba46b489723ab446
        "container-image": "docker://envoyproxy/envoy-build-ubuntu@sha256:6996521022f9dcd3fcf88ca3d44256f6c98712896e50815a79360791e0a174e6",
        "OSFamily": "Linux",
        "Pool": "linux",
    },
)

platform(
    name = "platform-asan",
    parents = ["@local_config_platform//:host"],
    constraint_values = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
        "@bazel_tools//tools/cpp:clang",
    ],
    exec_properties = {
        # Please update both the commented tag and the sha256
        # b0ff77ae3f25b0bf595f9b8bba46b489723ab446
        "container-image": "docker://envoyproxy/envoy-build-ubuntu@sha256:6996521022f9dcd3fcf88ca3d44256f6c98712896e50815a79360791e0a174e6",
        "OSFamily": "Linux",
        "Pool": "linux",
        # Necessary to workaround https://github.com/google/sanitizers/issues/916, otherwise, dangling threads in the
        # docker container fail tests on teardown (example: https://github.com/envoyproxy/envoy-mobile/runs/3443649963)
        "dockerAddCapabilities": "SYS_PTRACE",
    },
)
