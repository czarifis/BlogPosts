# Installing Windows 10 on VirtualBox



Recently Microsoft presented the Windows 10 OS. This is a pretty big deal if you consider that this OS is supposed to work on all hardware, from phones to tablets to PCs and so on.

>"But... But, I thought that Windows 8 was doing the same thing..." 

I hear you say... 

>"Yeah, right..."

I respond to that comment. So we'll find out if Windows 10 are any better.

So let's try to install it on a VM to find out if they are actually worth it. We will be using Windows 10 x64 but you can pick whatever version you want using [this](http://windows.microsoft.com/en-us/windows/preview-iso) link. 

Let's begin:

* Launch VitualBox

{<1>}![](/content/images/2014/10/image1.png)

* Select a name and pick Windows 8.1 64 bit (or 32 if you've downloaded the 32bit version)

{<2>}![](/content/images/2014/10/image22.png)

* Select 2048MB for the memory size. I tried to select 4096MB but for some reason when I was trying to install the OS the on the VM, it was aborting and this was the reason, so beware! 

{<3>}![](/content/images/2014/10/image3.png)

* Pick the "create new hard drive now" option 

{<4>}![](/content/images/2014/10/image4.png)

* Choose the VDI image. I guess it doesn't really matter what you pick, but since VirtualBox supports this image "natively" it's usually a better approach to use it.

{<5>}![](/content/images/2014/10/image5.png)

* Select the Dynamically allocated option

{<6>}![](/content/images/2014/10/image6.png)

* Pick a name for the drive and select the size you want

{<7>}![](/content/images/2014/10/image7.png)

OK good! Now launch the VM select the iso file you downloaded and follow the wizard to install Windows 10 on your VM.

Note! Choose the custom installation when the prompt appears and do the formatting yourself (just click on new). That way you'll avoid some issues that appear due to the fact that you're running this installation wizard on a VM.

