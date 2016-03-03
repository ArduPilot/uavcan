cmake_minimum_required(VERSION 2.8)

include_directories(include)

add_library(uavcan_stm32_driver STATIC
	src/uc_stm32_can.cpp
	src/uc_stm32_clock.cpp
	src/uc_stm32_thread.cpp
)

add_dependencies(uavcan_stm32_driver uavcan)

install(DIRECTORY include/uavcan_stm32 DESTINATION include)
install(TARGETS uavcan_stm32_driver DESTINATION lib)
