# for remote

## install ssh server and log in with ssh

- install openssh-server

```sudo apt install openssh-server```

- copy sshkeys

```copy-ssh-id xxx@xxx.xxx.xxx.xxx```

## open samba share

打开文件`\etc\samba\smb.conf`，增加响应配置（建议在`Share Definitions`行后面）
具体为：

``` conf
[display_folder_name]
    path = /home/pi/Shared
    public = no
    writeable = yes
    valid users = pi
```
