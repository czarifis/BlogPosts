# Installing NodeJS on Debian


Update your system:

	sudo apt-get update
    sudo apt-get install git-core curl build-essential openssl libssl-dev



	git clone https://github.com/joyent/node.git
    cd node
    
    
    
    git tag
    git checkout v0.10.32
    
    
    ./configure
    make
    sudo make install
    
    
## install npm

	curl -O -L https://npmjs.org/install.sh
    sudo sh install.sh
    
