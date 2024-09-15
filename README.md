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
Become root (sudo -i) then create and enter a directory download the Kernel version :  <br/>
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











<br /> Next enter the UI again, press / to enter the search function, and type fs  <br/>
<img src="https://github.com/user-attachments/assets/e1a812d1-0d8c-495a-995b-60cad686bd5a"/>
<img src="https://github.com/user-attachments/assets/0c5ea28b-88b5-4463-ba31-0a2adbadf9d4"/>
<br />
<br />
Press 2 to navigate to the filesystem configuration page and enable support for Btrfs and XFS by searching the page <br/>
<img src="https://github.com/user-attachments/assets/9edf200b-db58-4218-8f33-349d7381f664"/>
<img src="https://github.com/user-attachments/assets/35fb7b9b-932c-40c2-bdc6-c6cc306d8e6d"/>
</p>
<br />
<br />
Now use the exit at the bottom of the page back to the main screen and select Networking Support<br/>
<img src="https://github.com/user-attachments/assets/49654866-9e63-4559-841d-9a4ac4eb5468"/>
<br />
<br />
Press enter to view the Networking Support page and press the / and search for IPv6 similar to the previous steps<br/>
<img src="https://github.com/user-attachments/assets/b474ac7d-5701-42f6-b1fc-0edbfeba755e"/>
<img src="https://github.com/user-attachments/assets/6668f076-f418-4110-b504-0529494a47ef"/>
<br /> Now press 1 and hit enter to configure support for IPv6  <br/> 
<img src="https://github.com/user-attachments/assets/76f9bd28-aba5-4b6a-93e7-85fc10e83d9e"/>
</p>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
</p>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
</p>
Enter text here:  <br/>
<img src=""/>
</p>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
</p>Enter text here:  <br/>
<img src=""/>
</p>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
</p>Enter text here:  <br/>
<img src=""/>
</p>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
</p>Enter text here:  <br/>
<img src=""/>
</p>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
</p>Enter text here:  <br/>
<img src=""/>
</p>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
<br />
<br />
Enter text here:  <br/>
<img src=""/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
