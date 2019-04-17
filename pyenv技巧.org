#+OPTIONS: ^:nil
#+HTML_HEAD: <link rel="stylesheet" type="text/css" href="http://gongzhitaao.org/orgcss/org.css" />


* pyenv技巧
** 安装pyenv和虚拟环境插件
#+BEGIN_SRC 
git clone --depth=1 https://github.com/yyuu/pyenv.git ~/.pyenv
git clone --depth=1 https://github.com/yyuu/pyenv-virtualenv.git ~/.pyenv/plugins/pyenv-virtualenv
#+END_SRC



** 环境变量
*** zsh下
#+BEGIN_SRC 
echo 'export PYENVROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'export PATH="$PYENVROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc
#+END_SRC

*** bash下
#+BEGIN_SRC 
echo 'export PYENVROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENVROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
#+END_SRC


** 利用国内源加速安装python版本
#+BEGIN_SRC 
v=3.5.2|wget http://mirrors.sohu.com/python/$v/Python-$v.tar.xz -P ~/.pyenv/cache/;pyenv install $v
#+END_SRC
或者去 http://mirrors.sohu.com/python/
下载指定版本的tar包放置在.pyenv/cache目录下， 然后执行pyenv install即可安装



** 创建虚拟环境
#+BEGIN_SRC 
pyenv virtualenv 2.7.10 env2710
#+END_SRC

** 激活虚拟环境
#+BEGIN_SRC 
pyenv activate env2710
#+END_SRC

** 在shell脚本中使用pyenv
   #+BEGIN_EXAMPLE
   eval "$(pyenv init -)"
   eval "$(pyenv virtualenv-init -)"
   pyenv activate someenv
   #+END_EXAMPLE

