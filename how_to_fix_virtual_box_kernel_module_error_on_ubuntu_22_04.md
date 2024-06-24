# How To Fix VirtualBox Kernel Module Error On Ubuntu 22.04

If you have just freshly downloaded VirtualBox on your Ubuntu 22.04 OS and you try to check your version or create a VM with tools like `vagrant` you're likely to get an error along the lines of:

![vbox_error](https://github.com/tuyojr/troubleshooter/blob/main/images/vbox_error.png)

As the output above suggests, you need to recompile the kernel module and install it by running and following the prompts that show up:

```SHELL
sudo /sbin/vboxconfig
```

![run_sbin_vboxconfig](https://github.com/tuyojr/troubleshooter/blob/main/images/vbox_error_4.png)
![prompt_1](https://github.com/tuyojr/troubleshooter/blob/main/images/vbox_error_2.png)
![prompt_2](https://github.com/tuyojr/troubleshooter/blob/main/images/vbox_error_3.png)

## Restart Your System

Next, you need to restart your system and permit the use of third-party drivers by enrolling the new `Machine-Owner Key` that has been generated from the step above.

![restart_screen_1](https://github.com/tuyojr/troubleshooter/blob/main/images/enroll_mok.jpg)
![restart_screen_2](https://github.com/tuyojr/troubleshooter/blob/main/images/enroll_mok_2.jpg)
![restart_screen_3](https://github.com/tuyojr/troubleshooter/blob/main/images/enroll_mok_3.jpg)
![restart_screen_4](https://github.com/tuyojr/troubleshooter/blob/main/images/enroll_mok_4.jpg)
![reboot](https://github.com/tuyojr/troubleshooter/blob/main/images/reboot.jpg)

After successfully restarting your system, open your terminal and confirm again the version of your VirtualBox, it should print only the version number and no extra message, go on and create those VMs!!!!

![virtualbox_version](https://github.com/tuyojr/troubleshooter/blob/main/images/virtualbox_install.png)
