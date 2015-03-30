
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

curl --user email:password https://api.bitbucket.org/1.0/repositories/ --data name=REPO_NAME --data is_private='true' -v

git init
git add .
git commit -am 'initial'
curl -u "$username:$token" https://api.github.com/user/repos -d '{"name":"'$repo_name'"}'
git remote add origin https://github.com/rhelsing/$repo_name.git
git push origin master

## HEROKU

rake assets:precompile RAILS_ENV=production
heroku run rake db:migrate

## SETUP NEW MACHINE

ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor

brew install git

brew install rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc  
echo 'eval "$(rbenv init -)"' >> ~/.bashrc  
exec $SHELL  
git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build  
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc  
exec $SHELL
rbenv install 2.1.2 -v
rbenv global 2.1.2
ruby -v

gem install bundler
gem install rails

brew install zsh
curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh

## CONVERT FLAC TO MP3

for file in *.flac
      ffmpeg -i $file -acodec libmp3lame (basename $file).mp3
      sleep 60
end

