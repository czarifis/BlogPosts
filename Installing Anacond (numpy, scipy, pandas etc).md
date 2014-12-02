# Installing Anaconda (numpy, scipy, pandas etc) 

Anaconda is one of the most used Python libraries. It's actually a collection of the most popular python packages used in science, math engineering and so on. If you intend to use python for scientific purposes I guarantee that sooner or later you are going to need one or more of these packages. Additionally, manually installing one or more of these packages individually is usually a hard tasks due to dependency issues that arise. So let's begin then...

Oh btw, I am using Python 2.7...

follow [this](http://continuum.io/downloads) link to download the proper version for your OS. If you're using Ubuntu just copy the download URL open a terminal and do:

	wget http://09c8d0b2229f813c1b93-c95ac804525aac4b6dba79b00b39d1d3.r79.cf1.rackcdn.com/Anaconda-2.1.0-Linux-x86_64.sh # I'm just copying pasting the link here...

This might take a while so be patient...

When it's done do:
	
    bash Anaconda-2.1.0-Linux-x86_64.sh # Running the script

hit enter, press 'q' when the license appears, type yes and hit enter and enter if you want the default settings, when asked type "yes" to add the dependencies to your path.

cool now type:

	source ~/.bashrc
    
and you're done!

Type ipython into the terminal to verify that everything works (this actually checks only the iPython package but everything else should be alright as well)