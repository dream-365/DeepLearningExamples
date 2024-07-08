# Copyright (c) 2020, NVIDIA CORPORATION. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

ARG FROM_IMAGE_NAME=registry-vpc.cn-hangzhou.aliyuncs.com/hz-ns1/nvidia-tensorflow:20.10-tf1-py3

FROM ${FROM_IMAGE_NAME}

USER root

COPY requirements* ./
RUN pip install --no-cache-dir -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
RUN pip install --no-cache-dir --no-deps -r requirements-no-deps.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

WORKDIR  /wd
COPY . .