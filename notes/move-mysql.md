# move mysql data dir in ubuntu

## problem

recently I try to move data dir from `/var/lib/mysql` to other mounted disk  
it showes RW errors  

## solution

according to this website, I found a solution  
<https://blogs.oracle.com/jsmyth/apparmor-and-mysql>

```bash
systemctl restart apparmor # after changing the config file
```
