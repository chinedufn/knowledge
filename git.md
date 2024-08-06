Find replace:

```sh
# http://stackoverflow.com/a/21685766
git grep -lz 'subdomainA.example.com' | xargs -0 perl -i'' -pE "s/subdomainA.example.com/subdomainB.example.com/g"
```

## Commit history for a user

```
git log master --author="$(git config user.name)" --since=57.weeks --pretty=format:"%h - %an, %ad : %s"
```

## Git Lfs

Sometimes things go wrong and you get an Object no found error.

Removing it from git history can do the trick (make sure that's what we really want).

```
git lfs export -h
```

## Shell Aliases

#### Git aliases

```sh
git config --global alias.ch checkout
git config --global alias.cm commit
git config --global alias.br branch
git config --global alias.st status
git config --global alias.last log -1 HEAD
```

#### Shell Aliases

```
# Inside .zshrc

# Git
alias gs="git status"
alias gpoh="git push origin head"
alias gpch="git push cfn head"
alias gpm="git pull origin master"
alias gb="git branch"
alias gc="git commit"
# Print out the commits made since the tip of the master branch. (gnc stands for -> git new commits)
alias gnc="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%Creset' --abbrev-commit --date=relative master..head"
# Prevent git checkout from auto-completing branches on origin because it's almost never what I'm intending
export GIT_COMPLETION_CHECKOUT_NO_GUESS=1
```
