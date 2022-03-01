# This gives SHADOW_SOURCES and SHADOW_INCLUDE_PUBLIC_DIRS
include(${CMAKE_CURRENT_LIST_DIR}/Device-Shadow-for-AWS-IoT-embedded-sdk/shadowFilePaths.cmake)



set(DEVICE_SHADOW_INCLUDE_DIRS
    ${SHADOW_INCLUDE_PUBLIC_DIRS}
    ${CMAKE_CURRENT_LIST_DIR}/libraries/Device-Shadow-for-AWS-IoT-embedded-sdk/config
)


set(SHADOW_REQUIRES
)

idf_component_register(
    SRCS
        ${SHADOW_SOURCES}
    INCLUDE_DIRS
        ${DEVICE_SHADOW_INCLUDE_DIRS}
    REQUIRES
        ${SHADOW_REQUIRES}
)
