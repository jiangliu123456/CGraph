# 对应 example 中的内容
set(CGRAPH_EXAMPLE_LIST
        E01-AutoPilot
        E02-MockGUI
        E03-ThirdFlow
        E04-MapReduce
        E05-per_test
        )

foreach(example ${CGRAPH_EXAMPLE_LIST})
    add_executable(${example}
            $<TARGET_OBJECTS:CGraph>
            ${example}.cpp
            )
endforeach()
