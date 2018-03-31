file(GLOB_RECURSE srcs "*.cpp")
add_library(box2d STATIC ${srcs})
