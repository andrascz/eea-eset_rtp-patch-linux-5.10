# eea-eset_rtp-patch-linux-5.10

### !!! Use at your own risk !!!

Patch for Eset Endpoint Antivirus 7.1.9.0  with kernel >= 5.10

Module eset_rtp can not be compiled on kernels from 5.1, because `vfs_statat` in `linux/fs.h` moved out of line and not exported.

#### How to install

1. Install Eset Endpoint Antivirus 7.1.9.0

2. Download "ertp_handlers.c.patch" from this repository

3. Run in terminal ```cd /var/opt/eset/eea/eventd/eset_rtp/; sudo patch < __REPLACE_THIS_WITH_PATH_TO_DOWNLOADED_PATCH_FILE__```

4. Reboot

Tested with eicar sample - OK.

#### Additional info

It might also work with older EEA versions.
If you have kernel >= 5.8 you might need the [ertp_excludes.c.patch](https://github.com/voodoo-sys/ubuntu2010-eea-eset_rtp-patch) too

### !!! Use at your own risk !!!
