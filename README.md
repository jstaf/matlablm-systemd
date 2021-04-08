A systemd service template for MATLAB's FlexLM.

Just copy matlablm.service to `/etc/systemd/system/`. You need to change the `User` bit to a normal user on the machine in question (i.e. not root). Note that this is for a specific version of FlexLM installed in /usr/local/MATLAB. If installed in a different location, change the commands for `ExecStop` and `ExecStart` to the proper locations.

To start/stop FlexLM:

```
sudo systemctl start matlablm
sudo systemctl stop matlablm
```

To start on boot:

```
sudo systemctl enable matlablm
```
