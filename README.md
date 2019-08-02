*update_script* is a simple set of shell scripts to update one Freebsd's installation (world) and userland (ports). The script comes with a configuration file which can be 
edited in order to customize the update frequency, etc.  

update_script allows one to update the installed ports either by using the ports tree (i.e. make install clean) or the Freebsd's package manager (i.e. pkg). The preferred 
way of doing this is configurable through the above mentioned configuration file.
 
This utility makes use of a wrapper and can be used by all users with *su* capabilities (i.e. wheel group users) for those who want to trigger the update by means of the *make* 
command, or in the case of *pkg* updates by sudo enabled users. 

In addition to that, the update_wrapper can be automatically started by those making use of *openbox*   

### TODO

- [ ] Add .gitignore
- [ ] Add a check requirements function in the update_wrapper that checks for a user's privilege. If the user has no privilege, do not start the process. If yes, then call the update.
- [ ] Remove the logic for the update_wrapper for the scheduling of the "job" as we will leverage on cron scheduled scripts.
- [ ] Remove all the scheduler logic from the installer and add an insert into the cron schedule.