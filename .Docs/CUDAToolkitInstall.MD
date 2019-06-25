# CUDA Toolkit Install

The installation will mostly follow the official instrouction.

The official sites can be found from [here](https://developer.nvidia.com/cuda-downloads).

First we need to download the install file from official using `wget`.

```bash
root@HOSTNAME:~# wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/cu
da-repo-ubuntu1604_10.1.168-1_amd64.deb
--2019-06-25 17:09:43--  http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/cuda-repo-ubuntu1604_10.1.168-1_amd64.deb
Resolving developer.download.nvidia.com (developer.download.nvidia.com)... 192.229.232.112, 2606:2800:247:2063:46e:21d:825:102e
Connecting to developer.download.nvidia.com (developer.download.nvidia.com)|192.229.232.112|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2842 (2.8K) [application/x-deb]
Saving to: ‘cuda-repo-ubuntu1604_10.1.168-1_amd64.deb’

cuda-repo-ubuntu1604_10.1 100%[=====================================>]   2.78K  --.-KB/s    in 0s

2019-06-25 17:09:43 (101 MB/s) - ‘cuda-repo-ubuntu1604_10.1.168-1_amd64.deb’ saved [2842/2842]

root@HOSTNAME:~#
```

And we follow the official instrouction to read the .deb file with `~# dpkg -i cuda-repo-ubuntu1604_10.1.168-1_amd64.deb`.

```bash
root@HOSTNAME:~# dpkg -i cuda-repo-ubuntu1604_10.1.168-1_amd64.deb
Selecting previously unselected package cuda-repo-ubuntu1604.
(Reading database ... 26313 files and directories currently installed.)
Preparing to unpack cuda-repo-ubuntu1604_10.1.168-1_amd64.deb ...
Unpacking cuda-repo-ubuntu1604 (10.1.168-1) ...
Setting up cuda-repo-ubuntu1604 (10.1.168-1) ...

The public CUDA GPG key does not appear to be installed.
To install the key, run this command:
sudo apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/7fa2af80.pub

root@HOSTNAME:~#
```

Now, needs to fetch the keys to ensure the source and continue download package are correct, with `~# apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/7fa2af80.pub`.

```bash
root@HOSTNAME:~# apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/7fa2af80.pub
Executing: /tmp/tmp.6rYYkQMp85/gpg.1.sh --fetch-keys
http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/7fa2af80.pub
gpg: key 7FA2AF80: public key "cudatools <cudatools@nvidia.com>" imported
gpg: Total number processed: 1
gpg:               imported: 1  (RSA: 1)
root@HOSTNAME:~#
```

Now we can update the repository list for the softwares as `~# apt update`.

```bash
root@HOSTNAME:~# apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/7fa2af80.pub
Executing: /tmp/tmp.6rYYkQMp85/gpg.1.sh --fetch-keys
http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/7fa2af80.pub
gpg: key 7FA2AF80: public key "cudatools <cudatools@nvidia.com>" imported
gpg: Total number processed: 1
gpg:               imported: 1  (RSA: 1)
root@N-20HEPF0VLYJH:~# apt update
Ign:1 http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64  InRelease
Get:2 http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64  Release [564 B]
Get:3 http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64  Release.gpg [801 B]
Hit:4 http://archive.ubuntu.com/ubuntu xenial InRelease
Get:5 http://security.ubuntu.com/ubuntu xenial-security InRelease [109 kB]
Get:6 http://archive.ubuntu.com/ubuntu xenial-updates InRelease [109 kB]
Get:7 http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64  Packages [209 kB]
Get:8 http://archive.ubuntu.com/ubuntu xenial-backports InRelease [107 kB]
Fetched 536 kB in 4s (112 kB/s)
Reading package lists... Done
Building dependency tree
Reading state information... Done
All packages are up to date.
root@HOSTNAME:~#
```

Finally install the cuda toolkit with `~# apt install -y cuda-toolkit-10-1` command. And do not use cuda only if you knows what you are doing.

# CUDA Toolkitのインストール

# CUDA Toolkit 安裝
