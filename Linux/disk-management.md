### To view existing disk settings
````
lsblk
df -h (human readable form) -T (print the type) -l (local only)
du -h --max-depth=1 / (To View which folder/file is utilizing how much storage)
````
###  To extend an existing disk
````
sudo pvresize /dev/sda3
lvextend -l+100%FREE /dev/ubuntu-vg/ubuntu-lv
resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv
````
### To list Top 100 directories utilizing most amount of space
````
du -a /etc/ | sort -n -r | head -n 10
````
### To see the file system
````
df -T -h
df -T -h /data/
````
### Detailed report for Linux disk utilization
````
df -a
````