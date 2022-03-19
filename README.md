# exploretheworld



## 关于Docker的一些探索
默认情况下：
docker 的 volume 是可以让容器里进行读写同步在本机上，在本机上操作volume里面的内容也会在容器里面生效。

TODO:
- 探索一下Docker的网络相关内容。
- docker compose。
- 利用docker构建出一些提升开发效率的常用镜像出来。


## DockerFile 的一些指令解释

```
FROM       #基于基础镜像构建，一切从这里开始构建
MAINTAINER #镜像是谁写的，姓名+邮箱
RUN        # 镜像构建的时候需要运行的命令 
ADD        # 添加内容，文件内容等
WORKDIR    # 镜像的工作目录
VOLUME     # 挂载的目录
EXPOSE     # 暴漏的端口配置
CMD        # 指定这个容器启动的时候需要运行的命令，只有最后一个会生效
ENTRYPOINT # 指定这个容器启动的时候要运行的命令，可以追加命令
ONBUILD    # 当构建一个被继承 Dockerfile 这个时候就会运行 ONBUILD 的指令，触发指令。
COPY       # 类似 ADD，将文件拷贝到镜像中
ENV        # 构建的时候设置环境变量
```
