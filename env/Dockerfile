# our local base image
FROM ubuntu 

LABEL description="Container for use with Visual Studio" 

# install build dependencies 
RUN apt-get update && apt-get install -y g++ rsync zip openssh-server make gdb
# cmake ninja-build

# configure SSH for communication with Visual Studio 
RUN mkdir -p /var/run/sshd

RUN echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config  \ 
 && ssh-keygen -A 

# ----------------------------------------
# 參考資料
# ----------------------------------------
# - Build C++ Applications in a Linux Docker Container with Visual Studio
#   https://devblogs.microsoft.com/cppblog/build-c-applications-in-a-linux-docker-container-with-visual-studio/
# - How to setup an ssh server within a docker container
#   https://dev.to/s1ntaxe770r/how-to-setup-ssh-within-a-docker-container-i5i
# ----------------------------------------

# 建立帳號密碼 (skt90u / P@ssw0rd)
RUN useradd -m -d /home/skt90u -s /bin/bash -G sudo skt90u
RUN echo 'skt90u:P@ssw0rd' | chpasswd

# RUN service ssh start

# expose port 22 
EXPOSE 22

ENTRYPOINT service ssh restart && /bin/bash

# docker build -t ubuntu-vs .
# docker run -p 5000:22 -i -t ubuntu-vs /bin/bash
