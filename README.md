# cgl
Cross-platform OpenGL headers

# cmake example to link OpenGL library with project
```
if(WIN32)
    if(MSVC)
        target_link_libraries(${PROJECT_NAME} opengl32.lib)
    else()
        target_link_libraries(${PROJECT_NAME} -lopengl32)
    endif()
elseif(APPLE)
    find_package(OpenGL REQUIRED)
    target_link_libraries(${PROJECT_NAME} ${OPENGL_LIBRARIES})
else()
    target_link_libraries(${PROJECT_NAME} -lGL)
endif()
```
