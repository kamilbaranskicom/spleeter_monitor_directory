# spleeter_monitor_directory
Simple script monitoring directory and using spleeter to separate vocals and other tracks if new file detected.

## Usage
* Set `GLOBAL_SMD_PATH` and `PATH` to spleeter, ffmpeg, etc. (You can check the path with `which spleeter` and cutting the `spleeter` from result. You probably have spleeter already on `PATH`, but if you want to use spleeter_monitor_directory as a daemon, it might be required.)
* Run script with single argument: 2, 4 or 5 (number of stems).
* Copy WAV/MP3/AIFF/etc file to `GLOBAL_SMD_PATH/2stems/` and wait until the files will be ready in `GLOBAL_SMD_PATH/2stems/output/` .

## Daemon (instructions for Debian/Ubuntu)
* Move `spleetermd.service` to `/etc/systemd/system` .
* Update paths in `spleetermd.service` and `run` .
* Run `systemctl daemon-reload` (to update information for systemctl)
* Run `systemctl start spleetermd.service` (to run the daemon)
* Run `systemctl enable spleetermd.service` (to autorun with system)

## Requirements
* [spleeter](https://github.com/deezer/spleeter)
* [inotify-tools](https://github.com/inotify-tools/inotify-tools/wiki)
* bash