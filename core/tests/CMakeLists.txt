
add_executable(prometheus_core_test
  builder_test.cc
  check_label_name_test.cc
  check_metric_name_test.cc
  counter_test.cc
  family_test.cc
  gauge_test.cc
  histogram_test.cc
  registry_test.cc
  serializer_test.cc
  summary_test.cc
  text_serializer_test.cc
  utils_test.cc
)

target_link_libraries(prometheus_core_test
  PRIVATE
    ${PROJECT_NAME}::core
    GTest::gmock_main
)

add_test(
  NAME prometheus_core_test
  COMMAND prometheus_core_test
)
