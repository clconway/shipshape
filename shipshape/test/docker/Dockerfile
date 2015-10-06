# Copyright 2015 Google Inc. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# This docker image is for testing of Shipshape. It provides a ready-made
# environment in which Shipshape can be built and tested.
#
# Shipshape has the following build and test dependencies:
#
#  - Docker - Needed by Shipshape
#  - JDK version 8 - Needed by Bazel
#  - Bazel - Needed by Shipshape for building/testing
#  - Bison
#  - Clang
#  - Flex
#  - Go
#  - Android lint - Needed by Shipshape for testing
#
# Dependencies are listed at https://github.com/google/shipshape.
#

# -- Docker --
# This is a dind container and provides us with Docker
FROM gcr.io/shipshape_releases/dev_container:prod

# -- Shipshape --
RUN git clone --depth 1 https://github.com/google/shipshape.git
WORKDIR /shipshape
RUN ./setup_bazel.sh
