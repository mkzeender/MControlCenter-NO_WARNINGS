A fork of [MControlCenter](https://github.com/dmitry-s93/MControlCenter) that does not show warnings on every boot for missing drivers.

# MControlCenter

MControlCenter is a Free and Open Source GNU/Linux application that allows you to change the settings of MSI laptops.

![Screen Shot of MCC](https://github.com/user-attachments/assets/1e1dcb9b-aa8e-4410-8c77-f9554c1840cb)




## Features

 - CPU and GPU temperature display
 - Fan speed display
 - Switch between modes (Since version 0.2):
   - High Performance
   - Balanced
   - Silent
   - Super Battery
 - Change the maximum battery level limit
 - Advanced Fan Speed Control (Since version 0.4)
 - Change other settings such as keyboard backlight mode, USB Power Share, etc.


## Installation


### Installation from release


1. Download MControlCenter-x.x.x.tar.gz from the [releases page](https://github.com/mkzeender/MControlCenter-NO_WARNINGS/releases/)
2. Unpack the archive with the program
3. Open a terminal in the unpacked directory
4. Run the script `sudo ./install`
5. (Optional) `sudo ./uninstall` to uninstall

**Note:** Below are the steps for compiling, usually needed if your distrobution ships old versions of Qt6

### Building from source
After installing the main package (```qt6-base``` or ```libqt6widgets6```), you'll need to install other packages to build the app.

For ubuntru/Linux mint:
```qt6-base-dev``` and/or ```qt6-tools-dev``` also ```build-essential```

For Arch ```qt6-tools``` And for fedora ```qt6-qttools```

After you install the packages:

Make sure the app is completely closed if it was installed before (check if there is a system tray icon and close it).

Download the source code and extract the zip file.

Open the ```scripts``` folder.

Open a terminal inside the folder, then run these scripts in order:

1. ```build```
2. ```create installer```

If things went well, you should see a compressed file,

4. Extract it.
5. Open a terminal inside the new folder
6. Run the **UNINSTALL** script as *sudo*, it might fail if you don't have MCC installed. thats fine.
7. Run the **INSTALL** script as *sudo*, the last line should be a confirmation that the install was successful.
8. Check your apps, McontrolCenter should be there.

If the installation was successful but the app fails to run, open a terminal and type ```mcontrolcenter```, copy the output and open an issue (**IF** there isn't one already).

## Launch MControlCenter on session startup

To restore settings after a reboot, add MControlCenter to startup.

Execute this command on a terminal:

`cp /usr/share/applications/mcontrolcenter.desktop ~/.config/autostart/mcontrolcenter.desktop`

