# Start with System

To make the AI Kernel started with the system when Ubuntu OS boot up. Needs the systemd to trigger.

Also for the Python works and for debug(log) windows can be trace, decide to start the python script with screen command.

First create scripts to one time open main AWWW_web.py server script, create two scripts below.

`# vim Start_SV_NoTag.sh`

```bash
#start NoTag chatbot Python Server
cd /path/to/Chatbot-Server/NoTag/
source /root/.bashrc
python3 AWWW_web.py
```

`# vim Start_SV_WithTag.sh`

```bash
#start WithTag chatbot Python Server
cd /path/to/Chatbot-Server/WithTag/
source /root/.bashrc
python3 AWWW_web.py
```

Then we needs to make the scripts can be execute, add the attribute to the sh files.

`# chmod +x Start_SV_*.sh`

After this prepration, we needs to create a script execute above start-server script with screen command for the custom service running.

Here call it 'start-all.sh'. for the service been correctly referenced this script, we create it under '/usr/bin/'.

`# cd /usr/bin/`

`# vim start-all.sh`

```bash
#start all shell script
cd /path/to/Start_SV_*.sh/
screen -S NoTagServer -d -m /path/to/Start_SV_*.sh/Start_SV_NoTag.sh
screen -S WithTagServer -d -m /path/to/Start_SV_*.sh/Start_SV_WithTag.sh
```

And needs to let start-all.sh been executable.

`# chmod +x start-all.sh`

Finally create the custom service for python server scripts and NVidia DIGITS to run on startup.

Needs to create in both '/lib/systemd/system/' and '/etc/systemd/system/'.

`# cd /lib/systemd/system/`

`# vim aikernel.service`

```bash
[Unit]
Description=AIkernel use service.

[Service]
Type=forking
ExecStart=/bin/bash /usr/bin/start-all.sh

[Install]
WantedBy=multi-user.target
```

`# vim digits.service`

```bash
[Unit]
Description="Start NVidia DIGITS server. port 5000."

[Service]
Environment=PATH=/usr/local/cuda-10.1/bin/:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games$
Environment=CAFFE_ROOT=/root/caffe
Environment=LD_LIBRARY_PATH=/usr/local/cuda-10.1/bin/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
ExecStart=/bin/bash /path/to/DIGITS/digits-devserver
WorkingDirectory=/path/to/DIGITS/

[Install]
WantedBy=multi-user.target
```

Then make them both workable.

`# cp aikernel.service /etc/systemd/system/aikernel.service`

`# cp digits.service /etc/systemd/system/digits.service`

`# chmod 644 /etc/systemd/system/aikernel.service`

`# chmod 644 /etc/systemd/system/digits.service`

Test the service can normally start.

`# systemctl start aikernel`

`# systemctl start digits`

`# screen -ls`

`# ps aux | grep digits`

The last, if everything works properly, using enable to make it run with startup.

`# systemctl enable aikernel`

`# systemctl enable digits`

That's it!!

`=========================================================================`

# システムと一緒に実行

# 於系統開機時一起執行