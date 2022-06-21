cmake_minimum_required(VERSION 3.22)
project(socket C)

set(CMAKE_C_STANDARD 23)

# 生成服务端
add_executable(libevent_server server/server.c)
# 添加链接库
target_link_libraries(libevent_server event)

# 生成客户端
add_executable(libevent_client clent/clent.c)
# 添加链接库
target_link_libraries(libevent_client event)