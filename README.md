# update_script 
A Simple Script to update one's Freebsd installation. 

### Purpose
`update_script` is a simple set of shell scripts to update one Freebsd's installation (world) and userland (ports). The script comes with a 
configuration file which can be edited in order to customize the update frequency, etc. `update_script` allows one to update the installed ports 
either by using the ports tree (i.e. make install clean) or the Freebsd's package manager (i.e. pkg). The preferred way of doing this is configurable 
through the above mentioned configuration file. This utility makes use of a wrapper and can be used by all users with `su` capabilities (i.e. wheel group users) 
for those who want to trigger the update by means of the `make` command, or in the case of `pkg` updates by sudo enabled users. 

# How to use this set of scripts:
tbd

# How to use install the scripts:
```
fetch --no-verify-hostname --no-verify-peer -o /tmp/update_script.tgz https://api.github.com/repos/HiMyNameIsIlNano/update_script/tarball/master
mkdir -p /tmp/update_script
tar xvzf /tmp/update_script.tgz --strip=1 -C /tmp/update_script
cd /tmp/update_script
sh install
```