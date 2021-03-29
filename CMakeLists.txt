#Требуемая версия
cmake_minimum_required(VERSION 3.14...3.20 FATAL_ERROR) 

#Информация о проекте
project (
  Spline
  VERSION 0.1
  DESCRIPTION "Spline"
  LANGUAGES CXX
)

#Если является главным проектом, а не подпроектом
if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
    #C++
    set(CMAKE_CXX_EXTENSIONS OFF)
    set(CMAKE_CXX_STANDARD 14)
    
    #Разрешаем IDE работать
    set_property(GLOBAL PROPERTY USE_FOLDERS ON)

    #Включаем тестирование
    #include(CTest)
    
    #Включаем документирование
    #find_package(Doxygen)
    
    #if(Doxygen_FOUND)
        #add_subdirectory(docs)
    #else()
        #message(STATUS "Doxygen not found, not building docs")
    #endif()

endif()

#Добавляем папки
add_subdirectory(src)
add_subdirectory(apps)
