# Seting $JAVA_HOME environment variable

![Java icon](/content/images/2014/10/java.jpg)
If you're using linux for application development purposes, sooner or later you will have to use a tool that requires you to set the $JAVA_HOME environment variable. I will assume that you have already installed the required java packages, if this is not the case download the required JDK libraries first.

OK, on your linux system access your profile file, in my case (Ubuntu) I use the .bashrc file but this is not the only profile file that can get sourced at each session. If this file is not there don't worry, we will create it. Run the following command on the terminal:

	which java

If a path doesn't show up you'll have to download the JDKs I mentioned before. In my case the path that showed up here was the following:

>/usr/bin/java

So the path we would like to add is (just remove the executable "java" file):

>/usr/bin

Copy that path and do this:

	vim ~/.bashrc
    
get to the end of the file and write this:

	export JAVA_HOME=/usr/bin

if "/usr/bin" is not the path you got after running the "which" command paste the corresponding path instead.

OK, We are almost done! Go ahead and source the bash file:

	source ~/.bashrc
    
and then run the following:

	echo $JAVA_HOME

If you did everything correctly you should see the same path you were seeing while running the "which java" command.

If that's the case, congrats, you're done! You just set your JAVA_ENVIRONMENT variable. :)

If not then go to the .bashrc file again remove the "export JAVA_HOME..." line and start over.