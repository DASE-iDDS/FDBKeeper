if (NOT TARGET ch_contrib::rapidjson)
    message (${RECONFIGURE_MESSAGE_LEVEL} "Not building keeper-bench due to rapidjson is disabled")
    return()
endif ()

clickhouse_add_executable(keeper-bench Generator.cpp Runner.cpp Stats.cpp main.cpp)
target_link_libraries(keeper-bench PRIVATE clickhouse_common_zookeeper_no_log)
if(ENABLE_FDB)
    target_link_libraries(keeper-bench PRIVATE clickhouse_common_foundationdb dbms)
else()
    target_link_libraries(keeper-bench PRIVATE dbms)
endif()
target_link_libraries(keeper-bench PRIVATE ch_contrib::rapidjson)
