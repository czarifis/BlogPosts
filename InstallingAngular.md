## Installing angular JS on a Debian server

First thing first if this is a fresh OS installation we need to refresh the local package index of our package manager...

	sudo apt-get update

when this is done we continue with the installation of nodeJS and the nodeJS package manager

	sudo apt-get install nodejs
    sudo apt-get install npm


If we want to get the latest version of NodeJS we could do the following:

	sudo apt-get install curl
    sudo npm cache clean -f
	sudo npm install -g n
	sudo n stable

Now we should be having the latest version of NodeJS. Now it's time for Grunt and bower

    sudo npm install -g grunt-cli
	npm install -g bower

Make sure that no error messages pop up.






