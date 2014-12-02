# Installing Docker on CrunchBang (Debian)

So I recently started messing around with Docker and I have to admit, I like it! It's lightweight, you can do stuff with a certain level of isolation and... Awhmahgahd! You don't have to keep cloning and/or installing and re-installing Operating Systems on VMs over and over again.

So let's try to install Docker on a Debian ([CrunchBang](http://crunchbang.org/)) server:

	echo deb http://get.docker.io/ubuntu docker main | sudo tee /etc/apt/sources.list.d/docker.list
	
    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9

	sudo apt-get update

	sudo apt-get install -y lxc-docker
    
The four lines that will change your life...  (thanks to [this](https://coderwall.com/p/wlhavw/installing-docker-0-8-on-debian-wheezy-in-60-seconds) guy).

