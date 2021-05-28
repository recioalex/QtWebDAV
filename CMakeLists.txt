cmake_minimum_required(VERSION 3.19)
project(qwebdav)
find_package(QT NAMES Qt6 Qt5 COMPONENTS Widgets Sql Concurrent Network Xml REQUIRED)
find_package(Qt${QT_VERSION_MAJOR} COMPONENTS
        Widgets Sql Concurrent Network Xml
        REQUIRED)
set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR})
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR})
add_subdirectory(qwebdavlib)
add_subdirectory(qwebdavlibExample)