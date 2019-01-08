# vmware 记录

## 设置固定ip
修改 /Library/Preferences/VMware Fusion/vmnet8/dhcpd.conf

在下面的信息后边加入配置  
####### VMNET DHCP Configuration. End of "DO NOT MODIFY SECTION" #######
```
	host osname {
		hardware ethernet 00:0C:29:58:BD:B0;
		fixed-address 192.168.2.10;
	}
```
```sh
sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --configure
sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --stop 
sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --start    
```
