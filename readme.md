# install ZSH terminal in ubuntu and further tweaking 
zsh become one of my favorite terminal. I am using zsh in my ubuntu last 2 years. It graphically amazing.I love its auto completion. I can easily manage all of my alias and path variable using .zshrc file.    

first we will install zsh by following command
~~~bash
sudo apt install zsh
~~~
After installing zsh now I have to configure by downloading ad installing oh-my-zsh configuration through curl or wget    

via curl
~~~bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
~~~
via wget
~~~bash
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
~~~

To make zsh as my default bash terminal following command we need to execute. (require restart machine in order to take effect)
~~~bash
chsh -s /bin/zsh
~~~


If you open ~/.zshrc file you will find default theme is
~~~bash
ZSH_THEME="robbyrussell"
~~~
I personally love agnoster so in my ~/.zshrc file I changed to ZSH_THEME="agnoster"

To make a alias in .zshrc file 
~~~bash
alias zshconfig="vi ~/.zshrc" 
alias zshconfig_alias="vi ~/.zsh_alias" 
~~~

I can make a file with load of alias and load to .zshrc by following
~~~bash
source ~/.zsh_alias 
~~~

### Install powerline font
zsh icon require power line font. following repo has 
```bash
cd
wget https://github.com/powerline/powerline/raw/develop/font/PowerlineSymbols.otf
wget https://github.com/powerline/powerline/raw/develop/font/10-powerline-symbols.conf
mv PowerlineSymbols.otf ~/.fonts/
mkdir -p .config/fontconfig/conf.d #if directory doesn't exists
```

### Clean fonts cache
```bash
fc-cache -vf ~/.fonts/
```

### Move config file
```bash
mv 10-powerline-symbols.conf ~/.config/fontconfig/conf.d/
```

### For visual tweaking terminal using lot of theme go to following link 
[https://github.com/Mayccoll/Gogh]( https://github.com/Mayccoll/Gogh )


















