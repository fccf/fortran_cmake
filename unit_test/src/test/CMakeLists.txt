
include_directories(${CMAKE_CURRENT_BINARY_DIR}/../../)
set(test_names
  test_hello1
  test_hello2
  )

foreach(test ${test_names})
  file(GLOB src ${CMAKE_CURRENT_SOURCE_DIR}/${test}/*.f90)
  add_executable(${test} ${src})
  target_link_libraries(${test} hello)
  add_test(${test} ${test})
endforeach()
