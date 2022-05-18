cmake_minimum_required(VERSION 2.9)
project(place1)
 
#set(CMAKE_CXX_STANDARD 11)
set(OpenCV_DIR opencv) # xxxx目录包含OpenCVConfig.cmake
# 寻找OpenCV库
find_package( OpenCV REQUIRED )
# 添加头文件
include_directories(  ${OpenCV_INCLUDE_DIRS}  )
link_directories(/opt/intel/openvino_2021/inference_engine/lib/intel64)
include_directories(/opt/intel/openvino_2021.4.752/inference_engine/include)


add_executable(place1 main.cpp) 
# 链接OpenCV库

target_link_libraries( place1 ${OpenCV_LIBS} inference_engine) #/opt/intel/openvino_2021.4.752/inference_engine/include/inference_engine.hpp


