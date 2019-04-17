# 国内源加速
```
http://pypi.douban.com/  豆瓣
http://pypi.hustunique.com/  华中理工大学
http://pypi.sdutlinux.org/  山东理工大学
http://pypi.mirrors.ustc.edu.cn/  中国科学技术大学
http://e.pypi.python.org 北京 五星推荐这个
```

如果想手动指定源，可以在pip后面跟-i 来指定源，比如用豆瓣的源来安装web.py框架：
```
pip install flask  -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com
```
或者
```
vi ~/.pip/pip.conf
然后写入如下内容并保存

[global]
trusted-host =  mirrors.aliyun.com
index-url = http://mirrors.aliyun.com/pypi/simple
```
## update所有包
```
pip freeze --local | grep -v '^\-e' | cut -d = -f 1  | xargs pip install -U
```

