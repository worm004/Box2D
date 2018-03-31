project (Testbed)
file(GLOB_RECURSE Testbed_srcs "*.cpp")
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(X11 REQUIRED)
find_package (Threads)
add_executable(Testbed ${Testbed_srcs})
include_directories( ${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS} ${X11_INCLUDE_DIRS})

target_link_libraries(Testbed box2d imgui glew glfw  ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${X11_LIBRARIES} ${CMAKE_THREAD_LIBS_INIT} ${CMAKE_DL_LIBS} ${X11_Xrandr_LIB} ${X11_Xcursor_LIB} ${X11_Xinerama_LIB})

