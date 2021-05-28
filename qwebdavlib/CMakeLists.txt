add_library(qwebdav SHARED
        qnaturalsort.cpp
        qnaturalsort.h
        qwebdav.cpp
        qwebdav.h
        qwebdav_global.h
        qwebdavdirparser.cpp
        qwebdavdirparser.h
        qwebdavitem.cpp
        qwebdavitem.h
)

target_link_libraries(qwebdav PUBLIC
        Qt${QT_VERSION_MAJOR}::Widgets
        Qt${QT_VERSION_MAJOR}::Sql
        Qt${QT_VERSION_MAJOR}::Concurrent
        Qt${QT_VERSION_MAJOR}::Network
        Qt${QT_VERSION_MAJOR}::Xml
        )
target_include_directories(qwebdav PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_definitions(qwebdav PRIVATE -DQWEBDAV_LIBRARY)
target_compile_definitions(qwebdav PRIVATE DEBUG_WEBDAV)
set_target_properties(qwebdav  PROPERTIES AUTOMOC ON

        )