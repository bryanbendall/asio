add_library(asio INTERFACE)
target_compile_definitions(asio INTERFACE ASIO_STANDALONE)
target_include_directories(asio INTERFACE include)

if (WIN32)
target_compile_definitions(asio INTERFACE _WIN32_WINNT=0x0601)
target_compile_definitions(asio INTERFACE NOGDI)
target_compile_definitions(asio INTERFACE NOUSER)
endif (WIN32)