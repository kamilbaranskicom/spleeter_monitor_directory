# spleeter_monitor_directory
Simple script monitoring directory and using spleeter to separate vocals and other tracks if new file detected.

## Usage
* Set `GLOBAL_SMD_PATH`.
* Run script with single argument: 2, 4 or 5 (number of stems).
* Copy WAV/MP3/AIFF/etc file to `GLOBAL_SMD_PATH/2stems/` and wait until the files will be ready in `GLOBAL_SMD_PATH/2stems/output/` .

## Requirements
* [spleeter](https://github.com/deezer/spleeter)
* [inotify-tools](https://github.com/inotify-tools/inotify-tools/wiki)
* bash