

set (SOURCES 
  callback_manager_tests.cpp
  case_insensitive_comparison_utils_tests.cpp
  connection_impl_tests.cpp
  http_sender_tests.cpp
  hub_connection_impl_tests.cpp
  hub_exception_tests.cpp
  logger_tests.cpp
  memory_log_writer.cpp
  signalrclienttests.cpp
  stdafx.cpp
  test_http_client.cpp
  test_transport_factory.cpp
  test_utils.cpp
  test_web_request_factory.cpp
  test_websocket_client.cpp
  url_builder_tests.cpp
  web_request_stub.cpp
  web_request_tests.cpp
  websocket_transport_tests.cpp
)

include_directories(
    ../../src/signalrclient)
 
add_executable (signalrclienttests ${SOURCES})

target_link_libraries(signalrclienttests gtest signalrclient ${CPPREST_LIB})
add_test(NAME signalrclienttests COMMAND signalrclienttests)
