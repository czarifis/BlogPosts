#How to resize a VM using VirtualBox

![VirtualBox](/content/images/2014/10/VirtualBox-on-Mac-Again.png)

If you're using VirtualBox chances are that at some you'll have to resize the disk image that is used by your VMs. Thankfully, this is a rather painless procedure so let's jump right into it.

Since we will be using the VBoxManage tool to perform the resizing of our disk image we need to work with VirtualBox's native format for such images, the .vdi format. So, if your VM is using a .vmdk file we need to switch to a .vdi format first:

	VBoxManage clonehd "source.vmdk" "cloned.vdi" --format vdi
	
Ok let's resize the .vdi file now:

	# 30 * 1024 = 30720 MB
	VBoxManage modifyhd "cloned.vdi" --resize 30720

Done, at this point we can mount the disk image back to the VM. If you prefer to work with mvdk files, run the following command:

	VBoxManage clonehd "cloned.vdi" "resized.vmdk" --format vmdk
	
Ok now let's mount the new hard drive image to the VM:

Right click on the vm (from VirtualBox), click on settings and storage, delete the old vmdk and replace it with the new one.

Additionally since we need to let the OS know that the drive is actually resized, so we will download gparted.iso

Add the iso to the cd drive by right clicking to the controller, select "Add CD/DVD Device", select the iso and boot from gparted. Then resize the hard drive, close gparted and shutdown.

Afterwards unmount the cd drive (right click on the VM/settings/storage click on gparted click on disk iconand click: "Remove disk from virtual drive") and launch the VM. 

Cool, that should do it! You know have a VM with more space.
