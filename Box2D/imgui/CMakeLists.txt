file(GLOB_RECURSE imgui_srcs "*.cpp")
add_library(imgui STATIC ${imgui_srcs})
