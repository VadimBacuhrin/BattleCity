cmake_minimum_required(VERSION 3.10) # 4.2.1 еще не существует в 2025 году

set(PROJECT_NAME BattleCity) # Убрана запятая

project(${PROJECT_NAME})
  
add_executable(${PROJECT_NAME} src/main.cpp)

# Сначала добавляем папку с библиотекой
add_subdirectory(external/glfw)

# Затем привязываем библиотеку к нашему исполняемому файлу
target_link_libraries(${PROJECT_NAME} glfw)
