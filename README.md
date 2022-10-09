安卓13+可尝试卡刷带13的zip。      
无法开机可尝试另一个。      
记得备份boot分区。      
启动后需要挂载cgroupfs:      
```
mount -t tmpfs -o mode=755 tmpfs /sys/fs/cgroup
mkdir -p /sys/fs/cgroup/devices
mount -t cgroup -o devices cgroup /sys/fs/cgroup/devices
```

注：容器中没网可通过在容器中执行以下脚本解决：
https://github.com/Moe-hacker/termux-container/blob/main/package-zh/data/data/com.termux/files/usr/share/termux-container/group_add.sh
