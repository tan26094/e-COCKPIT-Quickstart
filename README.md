# e!COCKPIT-Quickstart
>This repository conatins educational and instructional resources for e!COCKPIT, and is intended to get you up and running with e!COCKPIT fast and easy

Check out the starter kit for e!COCKPIT (hereafter e!C) [here](https://www.wago.com/global/d/12984).\
For unzipping, please use **7-zip** or **WinRAR**.


## Installation
<div align="left">
   <br>
  <img src="img\05_install_and_check_it_out.png" width="200"><br><br>
</div>

1. **Recommended steps before installing:**
   1. Temporarily deactivate Windows Firewall
   2. Temporarily deactivate Windows Antivirus
   3. Ensure to complete a potential or pending WindowsUpdate installations
   4. Ensure that the hard drive has enough space for e!COCKPIT installation


2. **Required steps before installation:**
   1. Run e!C update-installation within the e!C tool menu/environment.\
   or
   2. Download the e!C [update-installer](https://www.wago.com/global/requestDirectDownload?downloadFile=swreg_ecockpit) from Wago web and run it separately with `install as admin`  
   or
   3. Download the latest e!C [full-installer](https://wago.sharefile.eu/d-sd68a97c766646cb8) and run it separately with `install as admin`   


3. **Required steps in case of partly successful e!C installation:**
   1. Close all open instances of e!C
   2. Download the Microsoft tool [streams](https://docs.microsoft.com/en-us/sysinternals/downloads/streams)
   3. Open a command prompt and navigate to the path `C:\ProgramData\WAGO Software`
   4. Extract the downloaded ZIP file into the above folder
   5. At the command prompt, type the following command: `streams.exe`
   6. Confirm the license dialog if you have never used the tool before (the tool will exit afterwards).
   7. At the command prompt, enter the command: `streams.exe -s -d *.*`\
      You should now get some lines of output text
   8. Finally you can close the prompt, e!C should be usable again in the known quality

```
Brief explanation of the tool:
The tool mentioned above removes the ADS entries that lead to conflicts (ADS stands for *Alternate Data Stream* and is a marker that flags files as a *non-local resource* in the file system and therefore restricts access). This makes the affected files available again without restriction.
```

4. **Required steps in case of full e!C re-installation:**
   1. Deinstall e!C, using normal Windows Control Panel procedure
   2. Deinstall CoDeSys 3.5 kernel, using [MicrosoftFixitTool](https://support.microsoft.com/en-us/mats/program_install_and_uninstall)
   3. Run Windows => StartButton => Run =  `regedit.exe` Search + Delete all registry keys containing `WAGO CODESYS V3.5`. Delete the associated Windows installation-reference folder, typically: `C:\Windows\Installer\{9A30716D-...}"C:\Program Files (x86)\InstallShield Installation Information\{9A30716D-...}`
   4. Download latest e!C [full-installer](https://wago.sharefile.eu/d-sd68a97c766646cb8) and run it separately with `install as admin`    


## Repair
<div align="left">
   <br>
  <img src="img\06_repair.png" width="200"><br><br>
</div>

1. **Navigate to [this](https://support.microsoft.com/en-us/mats/program_install_and_uninstall) webpage**
   1. You should see a Windows support site that *fixes problems that block programs from being installed or removed*
2. **Download the troubleshooter**
   1. If you see the File Download box when you start downloading, click **Run** or **Open**
   2. If you are operating on Windows 7, save the file and run as administrator
3. **You will get something similar to this picture:**
<div align="center">
   <br>
  <img src="img\01_start.PNG"><br><br>
</div>

4. **Choose *next*, and you will get something similar to:**
<div align="center">
   <br>
  <img src="img\02_whats_your_problem_bro.PNG"><br><br>
</div>

5. **Choose *uninstall*, and you will get:**
<div align="center">
   <br>
  <img src="img\03_choose_something_for_gods_sake!.PNG"><br><br>
</div>

6. **Then choose *CODESYS*, and *uninstall* :**
<div align="center">
   <br>
  <img src="img\04_be_smart_dude.PNG"><br><br>
</div>
