PROJECT (StepperCPU)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

FILE(GLOB LIB_SRC "src/*.cpp")
if(UNIX)
  ADD_DEFINITIONS(--std=c++0x)
endif (UNIX)

INCLUDE_DIRECTORIES ("${PROJECT_SOURCE_DIR}/include")
INCLUDE_DIRECTORIES ("${PROJECT_SOURCE_DIR}/../femlib/include")
INCLUDE_DIRECTORIES ("${PROJECT_SOURCE_DIR}/../vecmath/include")
INCLUDE_DIRECTORIES ("${PROJECT_SOURCE_DIR}/../include")
INCLUDE_DIRECTORIES ("${PROJECT_SOURCE_DIR}/../linsolver/include/")
INCLUDE_DIRECTORIES ("${PROJECT_SOURCE_DIR}/../linsolver/include/pcgsolver")
INCLUDE_DIRECTORIES ("${PROJECT_SOURCE_DIR}/../MCCD/include")
ADD_LIBRARY (StepperCPU  ${LIB_SRC})
SET(LIB_TYPE STATIC)	#set the lib type
