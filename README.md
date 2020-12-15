Add_Existing_Project_To_Git.md
https://gist.github.com/alexpchin/102854243cd066f8b88e




Create a CMake Linux project in Visual Studio
https://docs.microsoft.com/en-us/cpp/linux/cmake-linux-project?view=msvc-160

Linux development with C++ in Visual Studio
https://devblogs.microsoft.com/cppblog/linux-development-with-c-in-visual-studio/

How to setup an ssh server within a docker container
https://dev.to/s1ntaxe770r/how-to-setup-ssh-within-a-docker-container-i5i

### 建立 Linux 開發環境

[Build C++ Applications in a Linux Docker Container with Visual Studio](https://devblogs.microsoft.com/cppblog/build-c-applications-in-a-linux-docker-container-with-visual-studio/)
cd env
docker build -t ubuntu-vs .
docker run -p 5000:22 -i -t ubuntu-vs /bin/bash

service ssh start
useradd -m -d /home/skt90u -s /bin/bash -G sudo skt90u 
passwd skt90u

### VS 專案設定 (CMAKE)

https://docs.microsoft.com/zh-tw/cpp/linux/cmake-linux-project?view=msvc-160

### VS 專案設定

https://www.youtube.com/watch?v=af-1hDfoRcg

https://devblogs.microsoft.com/cppblog/linux-development-with-c-in-visual-studio/