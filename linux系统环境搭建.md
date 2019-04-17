# zsh
```
git clone --depth=1 git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
ZSH_THEME="ys"
ichsh -s /usr/bin/zsh
```

# 查询并杀掉进程
```
ps auxww | grep 'celery worker' | awk '{print $2}' | xargs kill -9
```

# 查找
```
sudo find / -name helo.txt
```

# 查看本机开放哪些端口
```
nmap -sTU localhost
```
# 防火墙检测和开启
```
firewall-cmd --query-port=80/tcp --zone=public  #查询80端口是否开启
firewall-cmd --zone=public --add-port=80/tcp --permanent #添加80端口
firewall-cmd --zone=public --add-port=3306/tcp --permanent  #添加3306端口
```

# redis 匹配删除key
```
redis-cli  KEYS "prefix:*" | xargs redis-cli  DEL
```

# 查看本地端口的监听
```
lsof -iTCP -sTCP:LISTEN -n -P
```
