# yavdr-hardware-ps3remote
This package improves the usability of the PS3 BD Remote with yaVDR.
## ps3remote
ps3remote processes the input events of the kernel input device created for the PS3 BD Remote and outputs them with added key repeats using uinput in order to improve the usability when using eventlircd.

### pairing the PS3 remote
```
sudo bluetoothctl
# in the bluetoothctl shell:
power on
scan on
# press START + ENTER on your PS3 remote
# list devices, note the MAC address (replace <MAC> with the actual address in the commands below)
devices
# note that you can use tab-completion when entering the <MAC>
trust <MAC>
connect <MAC>
quit
```
