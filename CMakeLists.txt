cmake_minimum_required(VERSION 3.2)
PROJECT(expressionEvaluation)
INCLUDE_DIRECTORIES(include)
AUX_SOURCE_DIRECTORY(src DIR_SRCS)
SET(TEST_LINER_STRUCT ${DIR_SRCS})
if(CMAKE_COMPILER_IS_GNUCXX)
	ADD_COMPILE_OPTIONS(-std=c99 -g)
	message(STATUS "optional:-std=c99 -g")
endif(CMAKE_COMPILER_IS_GNUCXX)
ADD_EXECUTABLE(${PROJECT_NAME} ${TEST_LINER_STRUCT})