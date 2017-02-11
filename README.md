*update_script* is a simple set of shell scripts to update one Freebsd's installation (world) and userland (ports). The script comes with a configuration file which can be 
edited in order to customize the update frequency, etc.  

update_script makes use of a wrapper and can only be used by a user with *su* capabilities (i.e. wheel group users). 

In addition to that, the update_wrapper can be automatically started by those making use of *openbox*   
