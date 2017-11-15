# dots 
My Arch Linux Dots.

# Installing
Managed using a bare git repository. Instructions adapted from here: [Atlasssian Developer: The best way to store your dotfiles](https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/)

1. Commit an alias to your .bashrc or zsh (I use zsh):

	`echo 'alias dots="/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME"' >> $HOME/.zshrc`
 
2. Reload the shell setting using that alias.

`source ~/.zshrc`

3. Clone this repo.

`git clone --bare https://github.com/fischernet/dots.git $HOME/.cfg`  

4. Checkout the actual content from the bare repo to your $HOME

`dots checkout`

5. Suppress untracked files

`dots config --local status.showUntrackedFiles no` 
 

