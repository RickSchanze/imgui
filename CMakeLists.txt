project(imgui)

set(IMGUI_FILES
        imgui.cpp
        imgui_demo.cpp
        imgui_draw.cpp
        imgui_tables.cpp
        imgui_widgets.cpp
        backends/imgui_impl_opengl3.cpp
        backends/imgui_impl_glfw.cpp
)

add_library(${PROJECT_NAME} ${IMGUI_FILES})

target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR})
target_include_directories(${PROJECT_NAME} PUBLIC backends)

target_link_libraries(${PROJECT_NAME}
        glfw
)
