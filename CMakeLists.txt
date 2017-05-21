project(untitled1)

set(CMAKE_CXX_STANDARD 14)

set(SOURCE_FILES main.cpp)
add_executable(untitled1 ${SOURCE_FILES})
find_package( Boost COMPONENTS system filesystem context regex REQUIRED )

target_link_libraries(${PROJECT_NAME}
        -lfolly
	-lglog
	-lev #Works without libev
        ${Boost_LIBRARIES}
)
