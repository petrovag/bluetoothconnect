# bluetoothconnect — Expect script for (re)connectiing (buggy) device for linux

Some Bluetooth devices have occasional problems reconnecting. In this case it usually helps to remove - add - pair the device in sequence. This script tries to connect the device and if the attempt fails, it removes and adds the device again. In this case the device must be in discoverable mode.
The only argument passed to the program is the device name or, more precisely, any unique substring of the device name.You can find it out with the command "bluetoothctl devices".


The script depends on expect, bluetoothctl and optionally notify-send.  In debian you can install them with the command:aptitude install bluez expect libnotify-bin

