# Copyright (c) 2020, Fraunhofer IESE
# All rights reserved.
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions are
# met:
#
# 1. Redistributions of source code must retain the above copyright notice,
#    this list of conditions and the following disclaimer.
#
# 2. Redistributions in binary form must reproduce the above copyright
#    notice, this list of conditions and the following disclaimer in the
#    documentation and/or other materials provided with the distribution.
#
# 3. Neither the name of the copyright holder nor the names of its
#    contributors may be used to endorse or promote products derived from
#    this software without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
# "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
# TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR
# PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER
# OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
# EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
# PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
# PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
# LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
# NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
# SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
#
# Author: Matthias Jung

cmake_minimum_required(VERSION 3.10)

# Project Name
project(Ramulator)

# Configuration:
set(CMAKE_CXX_STANDARD 11 CACHE STRING "C++ Version")
set(DCMAKE_SH="CMAKE_SH-NOTFOUND")


add_executable(ramulator
    src/ALDRAM.cpp
    src/Cache.cpp
    src/Config.cpp
    src/Controller.cpp
    src/DDR3.cpp
    src/DDR4.cpp
    src/DSARP.cpp
    src/GDDR5.cpp
    src/Gem5Wrapper.cpp
    src/HBM.cpp
    src/LPDDR3.cpp
    src/LPDDR4.cpp
    src/Main.cpp
    src/MemoryFactory.cpp
    src/PCM.cpp
    src/Processor.cpp
    src/Refresh.cpp
    src/SALP.cpp
    src/StatType.cpp
    src/STTMRAM.cpp
    src/TLDRAM.cpp
    src/WideIO2.cpp
    src/WideIO.cpp
)

target_include_directories(ramulator
    PRIVATE src/
)