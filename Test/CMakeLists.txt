
set(target Test)
add_library(${target})
target_sources(${target} PRIVATE
    impl0.cpp
    impl1.cpp
)
target_compile_features(${target} PRIVATE cxx_std_26)
# target_link_libraries(${target} PRIVATE Simpleton-Engine)


find_package(EnTT CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE EnTT::EnTT)
find_package(SDL2 CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE SDL2::SDL2)
find_package(SDL2_image CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE SDL2_image::SDL2_image)
find_package(SDL2_mixer CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE SDL2_mixer::SDL2_mixer)
find_package(SDL2_ttf CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE SDL2_ttf::SDL2_ttf)
find_package(glm CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE glm::glm)
find_package(nlohmann_json CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE nlohmann_json::nlohmann_json)
find_package(OpenGL REQUIRED)
target_link_libraries(${target} PRIVATE OpenGL::GL)
find_package(GLEW REQUIRED)
target_link_libraries(${target} PRIVATE GLEW::GLEW)