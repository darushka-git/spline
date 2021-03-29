#Имя бинарного файла 
add_executable(app app.cpp)
#Версия с++
target_compile_features(spline PUBLIC cxx_std_14)
#Требуемая бибилиотека
target_link_libraries(app PRIVATE spline tinynurbs::tinynurbs)
