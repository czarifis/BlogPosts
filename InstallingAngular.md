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

Make sure that no error messages pop up. If they do try to run the command that caused the errors as a super user.


At this point we will go ahead and fork the AngularJS repo. If you don't have a Github account you should do that first... Go on I'm waiting!

...

OK, make sure you've installed git:
	sudo apt-get install git

let's clone the forked repo (instead of czarifis use your own username):

	git clone https://github.com/czarifis/angular.js.git
    
Great! Now, let's add the upstream just in case we need to download any updates and let's install angularJS


    cd angular.js

    # Add the main AngularJS repository as an upstream remote to your repository:
    git remote add upstream "https://github.com/angular/angular.js.git"

    # Install node.js dependencies:
    sudo npm install

If you don't have installed Java, now is the right time... We will install Java 7:

	sudo apt-get install python-software-properties
    sudo add-apt-repository ppa:webupd8team/java
    sudo apt-get update
    sudo apt-get install oracle-java7-installer




When this is done we will install the bower components and we will build AngularJS

	# Install bower components:
    bower install

    # Build AngularJS:
    grunt package



