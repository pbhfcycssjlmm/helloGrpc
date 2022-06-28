# 前置条件
按照指引编译安装好grpc： https://grpc.io/docs/languages/cpp/quickstart/

# CMakeLists.txt编写依据
- 指引中的cmake命令带了：-DCMAKE_PREFIX_PATH=$MY_INSTALL_DIR，因此在CMakeLists.txt中用了替代语句list(APPEND CMAKE_PREFIX_PATH "/home/$ENV{USER}/.local/bin")
- 按照指引运行HelloWorld的时候，发现CMake的输出信息是在../cmake/common.cmake的第三个判断分支输出的，因此直接复制common.cmake第三个判断分支的内容。
- 只需要做验证，因此foreach语句中只保留了greeter_client greeter_server
- 其他部分直接复制HelloWorld的CMakeLists.txt内容
