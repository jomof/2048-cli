cmake_minimum_required(VERSION 3.10)

include_directories(${ANDROID_NDK}/sources/android/cpufeatures)
add_subdirectory(third_party/SDL)
target_sources(SDL2 PUBLIC ${ANDROID_NDK}/sources/android/cpufeatures/cpu-features.c)
add_subdirectory(app/src/main/cpp)
