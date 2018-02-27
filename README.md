# kernel-alive

Collection of scripts that back up modules of currently used kernel after a kernel update to prevent some issues that happen after a kernel update. 

After a kernel update, the modules of the currently running kernel get deleted. Thus, they can't be loaded, which can cause some issues when those missing modules are needed. Modules backed up this way can still be loaded and used by the system if needed. Therefore, it helps the operating system to stay fully functional after a kernel update.

Please note that new version of the kernel will still only be used at the next boot.

(Created after this thread : https://forum.manjaro.org/t/reboot-required-notifier/29809
Took an idea found on Reddit)
