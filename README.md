# Linux-Kernel-Customization

<h2>Description</h2>
In order to improve system functionality and performance, this project involves extensive Linux kernel customization and optimization. It requires downloading the most recent stable version of the Linux kernel, customizing it to meet system and hardware requirements, and compiling the modified kernel. 
<br />
<img src="https://github.com/user-attachments/assets/3b14c04b-9b17-4887-bba6-637180f7e4c4"/>


<h2>Languages and Utilities Used</h2>

Bash

<h2>Environments Used </h2>

- <b>CentOS Linux release 8.5.2111
 10</b>

<h2>Project walk-through:</h2>


<p align="center">
Navigate to kernel.org : <br/>
<img src="https://github.com/user-attachments/assets/80490e12-f6fa-4819-9eaf-d230ff6c8cd4"/>
<br />
<br />
Copy the latest stable tarball link address :  <br/>
<img src="https://github.com/user-attachments/assets/b20539c3-9ecd-4fb4-8ebc-49496e8603be"/>
<br />
<br />
Run the following to make sure your machine has the necessary packages intstalled: <br/>
<img src="https://github.com/user-attachments/assets/30e15c77-0234-4927-8928-8a5ac0887e0b"/>
<img src="https://github.com/user-attachments/assets/bc28c1c2-e03b-43cf-866a-d62a8c9e94a0"/>
<br />
<br />
Become root and then create and enter a directory download to the Kernel version :  <br/>
<img src="https://github.com/user-attachments/assets/60e9637f-a9cc-4039-a1ca-8b9a2687200e"/>
<br />
<br />
Run the wget [link address] and confirm the tarball has been downloaded in the desired directory:  <br/>
<img src="https://github.com/user-attachments/assets/f1c4fdb0-3f5f-4070-8310-44c5c44b6e76"/>
  <img src="https://github.com/user-attachments/assets/58aebb3f-ac9e-48c9-b98d-364623567ae3"/>
<br />
<br />
Now extract the tarball in the desired directory:  <br/>
<img src="https://github.com/user-attachments/assets/63889853-9abf-4cb5-9808-cb7bc901d7b4"/>
<br />
<br />
Confirm extraction and enter the kernel directory:  <br/>
<img src="https://github.com/user-attachments/assets/1a8b1afa-843c-409d-871b-69453a914358"/>
<br />
<br />
 <br />
 <br />
Run make menuconfig (install make if not installed) and wait for kernel UI to appear:  <br/>
<img src="https://github.com/user-attachments/assets/6f160c43-bb97-40e9-91eb-f973061c98a3"/>
  <img src="https://github.com/user-attachments/assets/c8403eef-ae55-47cf-a2a6-cac5d33dae39"/>
<br />
<br />
Press save to save current kernel configuration:  <br/>
<img src="https://github.com/user-attachments/assets/98a10a5e-310f-44ac-bffd-e7618783062b"/>
<br />Enter default kernel configuration file name<br />
  <img src="https://github.com/user-attachments/assets/8cdb1401-d66a-4895-a747-00b7badca684"/>
<br />Confirm default kernel configuration file has been created and saved<br />
<img src="https://github.com/user-attachments/assets/1a94a24f-acb1-4c5b-8ef7-737053bb6f14"/>
<img src="https://github.com/user-attachments/assets/a27b18d0-0f18-4bbb-bcbb-37e5dcfb03df"/>
<br /> Next enter the UI again, select File systems and hit enter  <br/>
<img src="https://github.com/user-attachments/assets/a3213ac4-ccd1-416b-b31e-824374e0942d"/>
<br />
<br />
Now navigate to the File systems configuration page and enable support for Btrfs and XFS by scrolling down <br/>
<img src="https://github.com/user-attachments/assets/9edf200b-db58-4218-8f33-349d7381f664"/>
<img src="https://github.com/user-attachments/assets/35fb7b9b-932c-40c2-bdc6-c6cc306d8e6d"/>
<br />Real-time data, such as audio and video, can be separated into a dedicated disk area for optimal performance when using XFS options like Realtime subvolume support. This is especially helpful for applications that need to operate reliably. Consistency checks can be performed while the filesystem is online with XFS online metadata check support, guaranteeing more efficient production operation. Debugging support and verbose warnings provide logs and extra diagnostics for troubleshooting, but they may also cause performance overhead. <br/> <br/>Enabling POSIX ACLs for Btrfs gives it more precise file permission control than standard UNIX permissions. Debugging support and assertions assist in finding and fixing bugs or filesystem errors, while sanity tests check the filesystem upon loading to detect problems before they become significant. In order to detect corruption or inconsistency in the filesystem and help maintain its integrity, the ref verify tool counts references in metadata.
 <br/>
<br />
<br />
Now use the exit at the bottom of the page back to the main screen and select Networking Support<br/>
<img src="https://github.com/user-attachments/assets/49654866-9e63-4559-841d-9a4ac4eb5468"/>
<br />
<br />
Press enter to view the Networking Support page and press the / and search for IPv6<br/>
<img src="https://github.com/user-attachments/assets/b474ac7d-5701-42f6-b1fc-0edbfeba755e"/>
<img src="https://github.com/user-attachments/assets/6668f076-f418-4110-b504-0529494a47ef"/>
<br /> Now press 1 and hit enter to configure support for IPv6  <br/> 
<img src="https://github.com/user-attachments/assets/76f9bd28-aba5-4b6a-93e7-85fc10e83d9e"/>
<img src="https://github.com/user-attachments/assets/782378df-dd59-4ae4-ac6f-a50d006d2e61"/>
<br />The IPv6 options offer a number of refined networking features. With the help of segment routing header encapsulation support, packets can be encapsulated and routed using the segment routing protocol, providing IPv6 networks with flexible and effective routing. By using HMAC (Hash-based Message Authentication Code) to authenticate segment routing headers, Segment Routing HMAC Support increases security by guaranteeing the integrity and authenticity of traffic. The RPL protocol, which is designed for routing in low-power and lossy networks and is frequently used in sensor and Internet of Things networks, can be used thanks to RPL Source Routing Header Support. Finally, in-band operation and maintenance (IOAM) is made possible by IOAM Pre-allocated Trace Insertion Support, which aids in network performance monitoring and diagnostics by allowing trace data to be inserted into packets. <br />
<br />
<br />
Next exit and navigate to Processor type and features  <br/>
<img src="https://github.com/user-attachments/assets/6f1f4628-7951-45c3-9d98-1abc3bf2aec5"/>
<br />
<br /> Navigate the page to find and enable MCE <br/>
<img src="https://github.com/user-attachments/assets/25eb556f-84f2-4a2e-8ab2-5ff1c05a3671"/>
<img src="https://github.com/user-attachments/assets/fbfef63a-2147-4002-9677-913aea5cea37"/>
<br /> <br/>The features of Intel MCE (Machine Check Exception) offer vital assistance in managing hardware malfunctions in Intel processors. With this option, the kernel can identify, log, and manage hardware problems in real time, such as memory errors, cache failures, or overheating. By turning on Intel MCE, you can increase system reliability and possibly avoid crashes by allowing the system to react to hardware issues before they cause instability or corrupt data. Systems needing strong error handling, like workstations and servers with Intel hardware, must have this feature.
 <br/>
<br />
<br />
 Now exit and navigate to the Power Management and ACPI  <br/>
<img src="https://github.com/user-attachments/assets/afb16975-a885-44a8-b6de-c186e8862d10"/>
<br />
<br /> Select CPU frequency and scaling <br/>
<img src="https://github.com/user-attachments/assets/5e633feb-8a08-4bd2-b8f8-e9ee4fb03b51"/>
<br />
  <br/> Find and enable Processor Clocking Control Interface Driver <br />
<img src="https://github.com/user-attachments/assets/c1e4ddd0-21d4-480b-98d6-d0e99663dfc0"/>
<br /> <br/> The system can monitor and regulate the CPU's clocking frequency thanks to the Processor Clocking Control Interface driver. Through the use of this interface, the operating system can dynamically modify the clock speed of the processor to maximize both performance and power efficiency in response to workload demands. Systems that make use of this feature can increase processing power and energy efficiency by decreasing power consumption during idle periods and increasing performance when needed. <br/>
<br />
<br />
Return to the main page using exit and navigate to Security Options  <br/>
<img src="https://github.com/user-attachments/assets/8e4d996f-219e-49d4-9b8b-e9488accef17"/>
<br />
<br />
Make sure SELinux is enabled and select SELinux kernel debugging support  <br/>
<img src="https://github.com/user-attachments/assets/65199278-7802-43c0-ba35-1a439d8b4232"/>
<br/>Additional debugging features for SELinux (Security-Enhanced Linux) can be enabled with the SELinux Kernel Debugging Support option. When enabled, it offers thorough logging and diagnostic data about the application and enforcement of SELinux policies, assisting system administrators and developers in debugging security-related problems. This can be helpful in understanding SELinux behavior during policy development or in diagnosing access control issues. However, because of the additional logging and checks made, turning on this option might result in performance overhead. It is primarily advised for environments used for testing or development where thorough security debugging is required.
<br/>
<br/>
<br/>
<br /> Now exit to return to the main screen and select Kernel hacking <br/>
<img src="https://github.com/user-attachments/assets/2e2fe366-d2fc-4399-93f7-f9cd1d15938a"/>
<br />
<br />
<br />
Find and enable Debug Preemptible Kernel <br/>
<img src="https://github.com/user-attachments/assets/9dd7c512-c747-4054-8c53-186408309a8b"/>
<br />The preemptible kernel, which enables the kernel to interrupt ongoing tasks in order to react faster to higher-priority tasks, can be debugged using the Debug Preemptible Kernel option. By offering thorough logs and checks during kernel operations, turning this option on aids developers in the diagnosis and troubleshooting of kernel preemption-related issues. In real-time or low-latency systems, this is helpful for determining race conditions, latency problems, or other timing-related issues. <br/> 
<br/>
<br />
Exit and navigate to Device Drivers from the main screen and hit enter<br/>
<img src="https://github.com/user-attachments/assets/665631b5-f409-4243-9322-80d258c3a53b"/>
<br /> Find and enable MMD/SD/SDIO card support<br/>
<img src="https://github.com/user-attachments/assets/2b240b24-e8ab-4b95-a004-dc529e64b8ef"/>
<br /> Memory card interfaces such as MMC (MultiMediaCard), SD (Secure Digital), and SDIO (Secure Digital Input Output) can be supported by the kernel when the MMC/SD/SDIO Support option is enabled. These interfaces are frequently used to access external storage or peripheral devices in gadgets like tablets, smartphones, embedded systems, and cameras. By turning on this option, users can mount external memory cards, use SD-based storage, and connect to peripherals like Wi-Fi adapters and GPS modules that use the SDIO standard. The kernel can also communicate with MMC, SD, and SDIO devices. For systems that need to communicate with SDIO peripherals or removable storage, this feature is crucial. <br/> 
<br />
<br />
Click save to save the new kernel configurations to a new configuration file <br/>
<img src="https://github.com/user-attachments/assets/088d712c-4194-4270-9fda-a85a8333d430"/>
 <img src="https://github.com/user-attachments/assets/d92be623-9213-44b5-9696-701d593338a0"/>
<br />Confirm the new kernel file contents <br/>
 <img src="https://github.com/user-attachments/assets/90672a83-406d-4fa8-8092-02fceb52da64"/>
<br />
<br />
Move the new kernel .config file to .config and execute the following <br/>
<img src="https://github.com/user-attachments/assets/97a94faa-6cef-4106-ba5d-22dde72fdcb7"/>
<br /> Confirm its contents <br/>
<img src="https://github.com/user-attachments/assets/26169f70-1b71-479e-904e-5ecdfeb9fecb"/>
<img src="https://github.com/user-attachments/assets/fbfc8441-26a3-4b7e-83d7-4a0dd4feafc3"/>
<br />
<br />
<br />
Cd into the .config source dir and run make modules to compile the kernel with modules  <br/>
<img src="https://github.com/user-attachments/assets/cb62d464-32a0-48ad-9ebf-df5ac1e6b10f"/>
<br />
<br />
 Confirm the results from the compiled kernel <br/>
<img src="https://github.com/user-attachments/assets/1280fd8e-8b85-4091-a283-546608ec70b2"/>
 <img src="https://github.com/user-attachments/assets/b9df3a35-f54c-4e1a-bc05-01bf13c4ad66"/>
<br /> Next run make modules_install && make install   <br/>
<img src="https://github.com/user-attachments/assets/8d675ab4-384b-465f-aaef-db9afcc4c8e0"/>
<br />
<br />
<br />
Verify that initrmfs was successfully created  <br/>
<img src="https://github.com/user-attachments/assets/c47f9d91-4893-4d75-b832-fee6339cc1ed"/>
<br />
<br />
Next update the grub configuration to include the new kernel. Check /boot to confirm <br/>
<img src="https://github.com/user-attachments/assets/b29ec83e-b78a-4766-a39a-ca04abaf951a"/>
<img src="https://github.com/user-attachments/assets/cba04c33-3231-4b1d-9a05-53de5738545b"/>
<br />
<br /> Quickly run uname -r to confirm current kernel release <br/>
<img src="https://github.com/user-attachments/assets/49b57d92-8823-4ebb-a5d2-1666c45cd1b5"/>
<br />
<br /> <br /> Now reboot and select desired custom kernel <br/>
<img src="https://github.com/user-attachments/assets/b4b2f462-4569-474e-bdbf-1f513f10d6c1"/>
<br/>Now run uname -r to confirm new kernel version <br/>
 <img src="https://github.com/user-attachments/assets/09dc9b70-c77a-42bd-aacb-3f8f79073a97"/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br /><br />  <br/>
<img src=""/>
<br />
<br />
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
