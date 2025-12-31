cmake_minimum_required(VERSION 3.10 FATAL_ERROR)

project(Glad)

# Создаём статическую библиотеку из файла glad.c
add_library(glad STATIC src/glad.c)

# Указываем, что заголовочные файлы находятся в папке include
target_include_directories(glad PUBLIC include)
