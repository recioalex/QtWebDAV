add_executable(qwebdav-example
        main.cpp
        qexample.cpp
        qexample.h
        )

target_link_libraries(qwebdav-example PRIVATE qwebdav)
set_target_properties(qwebdav-example  PROPERTIES AUTOMOC ON

        )