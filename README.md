# kernel-alive-openrc for artix

Forked from manjaro's kernel-alive. A collection of scripts that back up modules of currently running kernel after a kernel update to prevent some issues that happen after a kernel update. 

After a kernel update, the modules of the currently running kernel are deleted. Thus, they can't be loaded, which can cause some issues when those missing modules are needed. Modules backed up this way can still be loaded and used by the system if needed. Therefore, it helps the operating system to stay fully functional after a kernel update.

Its written for Artix-OpenRC with the ability to create boot option for different kernel versions.

Note:
The below files may not be needed.
  linux-module-cleanup.conf
  linux-module-cleanup.script
