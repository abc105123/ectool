file(GLOB_RECURSE sources
        CONFIGURE_DEPENDS *.cpp
)

target_sources("${PROJECT_NAME}" PRIVATE "${sources}")