# CMakeList.txt: wsl_debug 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
#
cmake_minimum_required (VERSION 3.9)

# 如果支持，请为 MSVC 编译器启用热重载。
if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

project ("wsl_debug")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/fft)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/cuda-samples)