# 基于screen的简单deamon
```
#!/bin/sh

#添加本地执行路径
export LD_LIBRARY_PATH=./

while true; do
        #启动一个循环，定时检查进程是否存在
        server=`ps aux | grep api_user | grep SCREEN | grep -v grep`
        if [ ! "$server" ]; then
            #如果不存在就重新启动
            screen -dmS api_user ./bin/api_user -c conf/api_user.conf
            #启动后沉睡10s
            sleep 10
        fi
        #每次循环沉睡10s
        sleep 2
done
```
