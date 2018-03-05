dotOS  For Huawei Y635 LTE
=============================

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/dot

Next, naviate into that new directory via the terminal:

	cd ~/dot

To initialize your local repository using the Turbo ROM trees, use this command:

	repo init -u git://github.com/DotOS/manifest.git -b dot-n

Also add the local manifests:

	git clone https://github.com/msm2354/local_manifest dot-n .repo/local_manifests

Then sync up with this command:

	repo sync --force-sync
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/dot

Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ prebuilts/misc/linux-x86/ccache/ccache -M 50G

Third:

	. build/envsetup.sh
	brunch hwY635
