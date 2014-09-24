
## SSH

ls -al ~/.ssh
ssh-keygen -t rsa -C "ryanhelsing@gmail.com"
ssh-add ~/.ssh/id_rsa
pbcopy < ~/.ssh/id_rsa.pub

## CREATE SHELL SCRIPT

in a file:
	#!/bin/bash
	commands $1 #first parameter
	echo "Enter the file: "
	read FILENAME
	echo "Printing head of $FILENAME..."
	head $FILENAME
chmod 755 file

export PATH=$PATH:$(pwd) / set PATH $PWD $PATH

## GIT

curl -u "$username:$token" https://api.github.com/user/repos -d '{"name":"'$repo_name'"}'

## HEROKU

rake assets:precompile RAILS_ENV=production
heroku run rake db:migrate

## RAILS SETUP ON NEW MACHINE

xcode
gcc # if need command line tools
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor
curl -sSL https://get.rvm.io | bash -s stable --rails
make rvm a function

## .BASH_PROFILE

set PATH /Users/ryanhelsing/Projects/bash/* $PATH
export PATH=$PATH:/Applications/Other/calibre.app/Contents/MacOS

#RVM LOAD IN FISH

if test -z $rvm_bin_path
  exec bash --login -c "exec fish"
end

