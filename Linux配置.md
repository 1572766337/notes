# 配置zsh
```
yum install zsh -y #安装zsh
chsh -s /bin/zsh #将zsh设置成默认shell（不设置的话启动zsh只有直接zsh命令即可）
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
# 下载插件
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
# 修改
vi ~/.zshrc
export ZSH="$HOME/.oh-my-zsh"
plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
ZSH_THEME="agnoster"
source $ZSH/oh-my-zsh.sh
alias vi=vim
```

# 配置vim
```
# 下载插件
git clone https://github.com/ervandew/supertab ~/.vim/supertab
git clone https://github.com/preservim/nerdtree ~/.vim/nerdtree
cp -r ~/.vim/supertab/* ~/.vim/
cp -r ~/.vim/nerdtree/* ~/.vim/
# 配置vim
vi ~/.vimrc
set nu
set ts=4
set et
set ai
set mouse=a
map <F2> :NERDTreeToggle<CR>
```
