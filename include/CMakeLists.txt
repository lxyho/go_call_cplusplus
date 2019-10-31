cmake_minimum_required(VERSION 3.0)
project(video)

aux_source_directory(. DIR_SRCS)
add_library(${PROJECT_NAME} SHARED ${DIR_SRCS})

if(WIN32)
  install(TARGETS ${PROJECT_NAME}
    RUNTIME DESTINATION lib)
else()
  install(TARGETS ${PROJECT_NAME}
    LIBRARY DESTINATION lib)
endif()  