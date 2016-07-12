## Getting Started ##
---------------

To get started with OMNI sources to build TWRP, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

To initialize your local repository using the KREMULTIROM trees to build TWRP-MULTIROM, use a command like this:

    repo init -u git://github.com/kremultirom/manifest_twrp_mrom_omni.git -b mrom-6.0
    
To initialize a shallow clone, which will save even more space, use a command like this:

    repo init --depth=1 -u git://github.com/kremultirom/manifest_twrp_mrom_omni.git -b mrom-6.0

Then to sync up:

    repo sync

Then git clone the device trees you need:

    cd <device-vendor-dir>; git clone https://github.com/kremultirom/device_lge_hammerhead hammerhead

Then to build:

     cd <source-dir>; . build/envsetup.sh; lunch omni_<device>-userdebug; mka recoveryimage
