#Подключаем файлы
set(
    HEADER_LIST 
    "${PROJECT_SOURCE_DIR}/include/spline/integral.hpp" 
    "${PROJECT_SOURCE_DIR}/include/spline/diff.hpp"
    )
    
add_library(spline integral.cpp diff.cpp ${HEADER_LIST})
target_include_directories(spline PUBLIC ../include)

#Версия С++
target_compile_features(spline PUBLIC cxx_std_14)

#Подключаем сторонние библиотеки
target_link_libraries(spline PRIVATE tinynurbs::tinynurbs)

#Для IDE
source_group(
  TREE "${PROJECT_SOURCE_DIR}/include"
  PREFIX "Header Files"
  FILES ${HEADER_LIST})
