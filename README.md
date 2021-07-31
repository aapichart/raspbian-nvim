#This is the neccessary configuration for ohmyzsh, nvim, tmux, ranger(cli file explorer)

  0.Install font - from the here (https://github.com/ryanoasis/nerd-fonts.git)
  
  1.ohmyzsh
    > sudo apt install curl zsh
    
    > sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

  2.nvim (This package need 0.3 or above)
    > sudo add-apt-repository ppa:neovim-ppa/stable
    > sudo apt update
    > sudo apt install neovim
    > nvim -version (This should show version above 0.3)
    
  3.nodejs - (in order to use neoclide/coc.vim package, we need nodejs newer than version 10)
    > curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
    
    > sudo apt install -y nodejs
    
    > sudo apt install npm
  
  4.tmux
    > sudo apt install tmux

  5.ranger
    > sudo apt install ranger
 
  6.fzf 
    > git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
    
    > ~/.fzf/install
    > build fd first
    > wget https://github.com/sharkdp/fd/releases/download/v7.3.0/fd-musl_7.3.0_amd64.deb
    > sudo dpkg -i fd-musl_7.3.0_amd64.deb
    
    > Then put this command into .zshrc file for autoload
    > [ -f ~/.fzf.zsh ] && source ~/.fzf.zsh
    > export FZF_DEFAULT_OPS="--extended"
    > export FZF_DEFAULT_COMMAND="rg --files --no-ignore-vcs --hidden"
    > export FZF_CTRL_T_COMMAND="$FZF_DEFAULT_COMMAND"

    information ->  https://codeyarns.com/tech/2017-10-24-how-to-install-and-use-fzf.html
    
  7.Install pip and virtualenv
    > sudo apt install python3-pip
    > pip3 install virtualenv
    
  8.ripgrep -> (rg) searching app for using with fzf
    > sudo add-apt-repository ppa:x4121/ripgrep
    > sudo apt-get update
    > sudo apt-get install ripgrep
  
  9.coc-vim
    > This is a plugin in nvim (written by nodejs)
    > It will automatically install 5-6 more extentions listed in ~/.config/nvim/general/setting.vim
    > ex. coc-prettier, coc-eslint, coc-json, coc-vim
    > We can manual install it on vim by using vim commane ":CocInstall coc-prettier"
    > 
    > In order to set coc-prettier and coc-eslint, please take a look at this url
    > https://dev.to/viclafouch/publish-your-own-eslint-prettier-config-for-react-projects-on-npm-g3p
