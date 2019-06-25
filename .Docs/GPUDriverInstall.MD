# GPU Driver Install

It is suggest to add official compitable ppa fo graphics-drivers install.

It only tested with NVidia GPU in this project.

Issue with command`~# add-apt-repository ppa:graphics-drivers/ppa` to add repository.

```bash
root@HOSTNAME:~# add-apt-repository ppa:graphics-drivers/ppa
 Fresh drivers from upstream, currently shipping Nvidia.

## Current Status

Current long-lived branch release: `nvidia-410` (410.66)
Dropped support for Fermi series (https://nvidia.custhelp.com/app/answers/detail/a_id/4656)

Old long-lived branch release: `nvidia-390` (390.87)

For GF1xx GPUs use `nvidia-390` (390.87)
For G8x, G9x and GT2xx GPUs use `nvidia-340` (340.107)
For NV4x and G7x GPUs use `nvidia-304` (304.137) End-Of-Life!

Support timeframes for Unix legacy GPU releases:
https://nvidia.custhelp.com/app/answers/detail/a_id/3142

## What we're working on right now:

- Normal driver updates
- Help Wanted: Mesa Updates for Intel/AMD users, ping us if you want to help do this work, we're shorthanded.

## WARNINGS:

This PPA is currently in testing, you should be experienced with packaging before you dive in here:

Volunteers welcome!

### How you can help:

## Install PTS and benchmark your gear:

    sudo apt-get install phoronix-test-suite

Run the benchmark:

    phoronix-test-suite default-benchmark openarena xonotic tesseract gputest unigine-valley

and then say yes when it asks you to submit your results to openbechmarking.org. Then grab a cup of coffee, it takes a bit for the benchmarks to run. Depending on the version of Ubuntu you're using it might preferable for you to grabs PTS from upstream directly: http://www.phoronix-test-suite.com/?k=downloads

## Share your results with the community:

Post a link to your results (or any other feedback to): https://launchpad.net/~graphics-drivers-testers

Remember to rerun and resubmit the benchmarks after driver upgrades, this will allow us to gather a bunch of data on performance that we can share with everybody.

If you run into old documentation referring to other PPAs, you can help us by consolidating references to this PPA.

If someone wants to go ahead and start prototyping on `software-properties-gtk` on what the GUI should look like, please start hacking!

## Help us Help You!

We use the donation funds to get the developers hardware to test and upload these drivers, please consider donating to the "community" slider on the donation page if you're loving this PPA:

http://www.ubuntu.com/download/desktop/contribute
 More info: https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa
Press [ENTER] to continue or ctrl-c to cancel adding it
```

When saw this notification, press <kbd>Enter ⏎</kbd> to continue.

```bash
gpg: keyring `/tmp/tmped97551c/secring.gpg' created
gpg: keyring `/tmp/tmped97551c/pubring.gpg' created
gpg: requesting key 1118213C from hkp server keyserver.ubuntu.com
gpg: /tmp/tmped97551c/trustdb.gpg: trustdb created
gpg: key 1118213C: public key "Launchpad PPA for Graphics Drivers Team" imported
gpg: no ultimately trusted keys found
gpg: Total number processed: 1
gpg:               imported: 1  (RSA: 1)
OK
root@HOSTNAME:~#
```

Then we need to issue `~# apt update` to refresh the list of what packages can be installed.

```bash
root@HOSTNAME:~# apt update
Get:1 http://ppa.launchpad.net/graphics-drivers/ppa/ubuntu xenial InRelease [24.3 kB]
Hit:2 http://archive.ubuntu.com/ubuntu xenial InRelease
Hit:3 http://security.ubuntu.com/ubuntu xenial-security InRelease
Get:4 http://archive.ubuntu.com/ubuntu xenial-updates InRelease [109 kB]
Get:5 http://archive.ubuntu.com/ubuntu xenial-backports InRelease [107 kB]
Get:6 http://ppa.launchpad.net/graphics-drivers/ppa/ubuntu xenial/main amd64 Packages [14.9 kB]
Get:7 http://ppa.launchpad.net/graphics-drivers/ppa/ubuntu xenial/main Translation-en [4,572 B]
Fetched 260 kB in 7s (34.6 kB/s)
Reading package lists... Done
Building dependency tree
Reading state information... Done
42 packages can be upgraded. Run 'apt list --upgradable' to see them.
root@HOSTNAME:~#
```

And then we can start install the corrispond GPU driver by issue `~# ubuntu-drivers autoinstall` command.

After the installation donw, use `~# nvidia-smi` to check the result. 

# GPU Driverのインストール

# GPU Driver 安裝
