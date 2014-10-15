# Launching a headless VM from the terminal using VirtualBox

So lately my VNC server decided that it's a good time for it to crash even though I have a paper deadline in 3 weeks and I'm still trying to develop some demo apps for it. Good times!

Anyways let's see how to run a VM using the CLI tools that come with VirtualBox.

List the names of your VMs that can be launched from VirtualBox:

	VBoxManage list vms

    # If you want a more verbose description do:
    # VBoxManage list vms --long

This is what I got in my case:

>"Ubuntu" {c5b78ec5-888d-4761-98e6-f59efe4e270c}

>"UbuntuVM" {2c0f7a39-45d9-46cd-8862-564dbf8539c3}

Cool! Now let's run the following:

	 startvm UbuntuVM --type headless 
     
The _"type headless"_ basically means that no window showing the actual running VM will appear (it will run on the background though, don't worry). This window would be useless anyways since we don't have a VNC server running, so let's save some resources. 

If you want to run a headless VM using VirtualBox's GUI press shift and click on the start button after having selected the VM you want to launch. It might come in handy at some point...

To power off the VM using the terminal do:

	VBoxManage controlvm UbuntuVM poweroff 
    
It is suggested to not power off the VM this way. Instead log in to the VM and shut it down.

That's all folks!
