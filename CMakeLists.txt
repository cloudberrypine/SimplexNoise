# Copyright (c) 2014-2018 Sebastien Rombauts (sebastien.rombauts@gmail.com)
#
# Distributed under the MIT License (MIT) (See accompanying file LICENSE.txt
# or copy at http://opensource.org/licenses/MIT)
cmake_minimum_required(VERSION 3.5)
if (CMAKE_VERSION VERSION_LESS "3")
    project(SimplexNoise CXX)
else()
    cmake_policy(SET CMP0048 NEW)
    project(SimplexNoise VERSION 1.0.0 LANGUAGES CXX)
endif()

cmake_minimum_required(VERSION 3.5)
# add the application executable
add_library(SimplexNoise ${PROJECT_SOURCE_DIR}/src/SimplexNoise.cpp ${PROJECT_SOURCE_DIR}/src/SimplexNoise.h)
target_link_libraries(SimplexNoise ${SYSTEM_LIBRARIES})
target_include_directories(SimplexNoise PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

