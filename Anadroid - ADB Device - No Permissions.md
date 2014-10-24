# Android - ADB Device - No Permissions 

So this error appears quite frequently if you're developing android applications on linux and you're using a physical device for testing purposes. Basically, it means that the Android Debug Bridge doesn't have permissions to access your device.

And here is how you fix that...

First try doing the following:

	
	adb kill-server
    adb start-server

If this doesn't fix the problem, navigate to the android SDK directory and run the following:

	cd /platform-tools
    sudo chown root:<yourUserGroup> adb
    sudo chmod 4550 adb
    ./adb kill-server
    ./adb start-server

If you've enable the USB debugging on your physical device, a popup is going to show up asking if you want to accept the USB connection, tap on OK and you're done!

Now the device should be good to go.