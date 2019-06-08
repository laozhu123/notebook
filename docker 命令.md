# docker 命令
1. docker top name 查看容器中运行的进程
2. docker exec name ps 查看进程PID
3. docker exec name kill <PID>
4. docker kill 和 docker rm -f 一样的效果
5. docker save 将镜像保存为文件
6. docker load 将文件加载进来
7. docker rm -v 删除容器并删除管理卷
8. docker port name 查看容器的端口映射
9. docker rm -vf 停止容器、删除容器和管理卷
10. docker inspect --format "{{.Config.User}}" name 查看容器以什么用户启动
11. docker diff name 查看容器中改变的文件
12. docker commit -a "username" -m "message" container-name new-image-version
13. docker run --name cmd-git --entrypoint git image 入口点设置后，exec运行的命令都是传参数给他
14. docker run image -c "echo helo" 设置默认命令
15. docker history image 查看镜像层历史
16. docker onbuild所传递的指令，在被继承时才使用
17. docker info 查看docker信息，如image和container数量

1. docker-compose 可以构建多个容器，完成系统的部署
2. docker-compose up -d 运行
3. docker-compose logs 查看日志
4. docker-compose up --no-dep -d proxy