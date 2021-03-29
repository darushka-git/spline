
set(DOXYGEN_EXTRACT_ALL YES)
set(DOXYGEN_BUILTIN_STL_SUPPORT YES)

doxygen_add_docs(
                 docs spline/integral.hpp "${CMAKE_CURRENT_SOURCE_DIR}/integral.md"
                 docs spline/diff.hpp "${CMAKE_CURRENT_SOURCE_DIR}/diff.md"
                 WORKING_DIRECTORY "${PROJECT_SOURCE_DIR}/include"
                 )
 
