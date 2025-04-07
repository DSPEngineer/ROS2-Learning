# Developer Environment

Lets be sure we have the right environment for the remaining tutorials, in the repository.

## Ubuntu 24.04
You should have Ubuntu 24.04. Type the following command:
```bash
lsb_release -a
```
You should get the following response:
```
    No LSB modules are available.
    Distributor ID:	Ubuntu
    Description:	Ubuntu 24.04.2 LTS
    Release:	24.04
    Codename:	noble
```
## ROS2 (Jazzy Jalisco):
You should have ROS2 Jazzy. Type the following command:

```bash
ls -al /opt/ros/jazzy
```
You should get the following response:
```
total 140
drwxr-xr-x   9 root root  4096 Jan  6 09:20 .
drwxr-xr-x   3 root root  4096 Jul 10  2024 ..
drwxr-xr-x   2 root root  4096 Mar 17 07:46 bin
drwxr-xr-x 123 root root  4096 Jan 16 08:02 include
drwxr-xr-x  87 root root 45056 Mar 17 07:46 lib
-rw-r--r--   1 root root   373 Apr 18  2024 local_setup.bash
-rw-r--r--   1 root root  3901 Dec 17 23:58 local_setup.sh
-rw-r--r--   1 root root 15895 Apr 18  2024 _local_setup_util.py
-rw-r--r--   1 root root   379 Apr 18  2024 local_setup.zsh
drwxr-xr-x  20 root root  4096 Sep 16  2024 opt
-rw-r--r--   1 root root   349 Apr 18  2024 setup.bash
-rw-r--r--   1 root root  4274 Dec 17 23:58 setup.sh
-rw-r--r--   1 root root   622 Apr 18  2024 setup.zsh
drwxr-xr-x 325 root root 20480 Jan 21 09:01 share
drwxr-xr-x   4 root root  4096 Jul 10  2024 src
drwxr-xr-x   3 root root  4096 Jul 10  2024 tools
```
## Test ROS2 installation:
If you have a ROS2 Jazzy installation, you should be able to source the _setup.bash_ file and run a few ROS2 commands. The setup command creates the "_underlay_", a basic set of commands and path to the standard ROS2 installed package(s).
```bash
source /opt/ros/jazzy/setup.bash
printenv ROS_DISTRO
```
If ROS2 Jazzy is properly installed, sourcing the _setup.bash_ file will change your PATH to include the following:
```
    -- /opt/ros/jazzy/opt/gz_msgs_vendor/bin
    -- /opt/ros/jazzy/opt/gz_tools_vendor/bin
    -- /opt/ros/jazzy/opt/gz_ogre_next_vendor/bin
    -- /opt/ros/jazzy/bin
```
Setup will also set a few ROS environment variables, one of which is ROS_DISTRO. You should see the following response to the _printenv_ command:
```
jazzy
```
The ROS2 _underlay_ provides the required build tools (colcon, cmake, etc.), package dependencies, libraries and other ROS2 packages. The _underlay_ (setup.bash) essentially enables the ROS2 development environment.

_**NOTE:**_ you will need to create a new _underlay_ for each terminal you intend to use for ROS development or testing. Be sure to source this file or add it to your "_.bashrc_" or "_.bash_aliases_" file.
