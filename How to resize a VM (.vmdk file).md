#How to resize a VM (.vmdk file)

If the VM is using a vmdk file we need to switch to a VDI format:

	VBoxManage clonehd "source.vmdk" "cloned.vdi" --format vdi
	
Ok let's resize it now:

	# 30 * 1024 = 30720 MB
	VBoxManage modifyhd "cloned.vdi" --resize 30720

Let's change the format back to .vmdk

	VBoxManage clonehd "cloned.vdi" "resized.vmdk" --format vmdk
	
Ok when this is done we we will need to use the new hard drive on VirtualBox:

Right click on the vm (inside virtualbox), click on settings and storage.

We will delete the old vmdk and replace it with the new one.

Additionally since we need to let the OS know that the drive is actually resized we will download gparted.iso

Add the iso to the cd drive by right clicking to the controller, select "Add CD/DVD Device", select the iso and boot from gparted. Then perform the resizing of the hard drive close gparted and shutdown.

Afterwards unmount the cd drive (right click on the VM/settings/storage click on gparted click on disk iconand click: "Remove disk from virtual drive") and launch the VM. That should do it!
