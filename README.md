

Installation:

    git clone git://github.com/HeikoR/Vim-files.git ~/vimfiles

Create symlinks:

    ln -s ~/.vim/vimrc ~/.vimrc
    ln -s ~/.vim/gvimrc ~/.gvimrc

    mklink /H %USERPROFILE%\_vimrc %USERPROFILE%\vimfiles\_vimrc
    mklink /H %USERPROFILE%\_vimrc_heiko %USERPROFILE%\vimfiles\_vimrc_heiko

Switch to the `~/.vim` directory, and fetch/update submodules:

    cd ~/.vim
    git submodule init
    git submodule update

Installing git submodule (e.g. fugutive plugin)

	cd ~/.vim
	mkdir ~/.vim/bundle
	git submodule add http://github.com/tpope/vim-fugitive.git bundle/fugitive
	git add .
	git commit -m "Install Fugitive.vim bundle as a submodule."

Upgrading a specific plugin bundle (e.g. fugitive plugin)

	cd ~/.vim/bundle/fugitive
	git pull origin master

Upgrading all bundled plugins

	git submodule foreach git pull origin master

	Note: if you get a libiconv-2.dll error, then copy this file from git\bin to git\libexec\git-core.

















