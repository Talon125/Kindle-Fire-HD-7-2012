# Kindle Fire HD 7" (2012)
Tate PVT 08

This is a discontinued Android-based tablet by Amazon. The latest system version
is 7.5.1. It runs Fire OS, this version being based on Android 4. This tablet
was the 2nd generation in the Fire Tablet series. The one I'm using has an
internal storage capacity of 16 GB.

```
shell@android:/ $ getprop ro.build.version.release
4.0.3
```

Read more about it:
- https://en.wikipedia.org/wiki/Fire_HD#Discontinued_Fire_HD_tablet_devices
- https://developer.amazon.com/docs/fire-tablets/ft-device-specifications-firehd-models.html?v=firehd7_2012
- https://en.wikipedia.org/wiki/Fire_OS

Should any of the links no longer be available, please visit the Internet
Archive at https://web.archive.org/.  
Should the Internet Archive be currently down, then you may find manually copied relevant info in
[Specifications_KindleFireHD7.md](Specifications_KindleFireHD7.md).

## Root (SuperSU)
Root (installs SuperSU app too) by manually entering `adb` commands in Linux.  
See [Guide_Root/README.md](Guide_Root/README.md)

## Backup
Before TWRP, make a backup using `dd`.  
See [Guide_Backup/README.md](Guide_Backup/README.md)

## TWRP (Team Win Recovery Project)
Flash TWRP 3.0.2 to the Kindle.  
See [Guide_TWRP/README.md](Guide_TWRP/README.md)

## Custom ROMs
I tried `crDroidAndroid-7.1.2-20181021-tate-v3.8.9.zip`, and it works! Except
for the camera, though. NewPipe (YouTube) runs fine on it, though the only
quality settings available for the videos is 360p? Not sure if that's because of
NewPipe or the OS or the Kindle.  
See [Guide_CustomROM/README.md](Guide_CustomROM/README.md)

## Nifty ADB commands
ADB = Android Debugging Bridge

https://techblogs.42gears.com/list-of-all-widely-used-adb-commands/

https://gist.github.com/Pulimet/5013acf2cd5b28e55036c82c91bd56d8

also see `/adb_command_help_texts/` (folder in this repo)

### List packages
```
pm list packages
```

### Start Camera
```
am start -n com.android.camera/.Camera
```

### Start Settings
```
am start -n com.android.settings/.Settings
```

### Go into Developer Options (Settings)
```
am start -a android.settings.APPLICATION_DEVELOPMENT_SETTINGS
```