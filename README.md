# Export visible devices
Shell script that exports GPUs that are not in use to the `CUDA_VISIBLE_DEVICES` environment variable.

## Installation & usage
First download the script and give execution permissions.
```sh
wget https://raw.githubusercontent.com/jppgks/export-visible-devices/master/export_visible_devices
chmod +x ./export_visible_devices
```
You can now use the script as follows (the command is `source`d to keep the variables set in the script):
```sh
source ./export_visible_devices
```

### Treshold
The script checks for the amount of memory in use on each GPU.
If it is lower than a treshold (defaults to 5), given in MB, it exports the GPU ID to the environment variable.

You can pass a different treshold using the `-t` option:
```sh
source ./export_visible_devices -t 2
```
