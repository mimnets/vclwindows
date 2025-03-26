# Custom Preinstalled Windows 11
## https://www.youtube.com/watch?v=jvSIa3OgMy4
 1. To Start Sysprep
    %windir%\system32\sysprep\sysprep.exe /audit /reboot
 2. To Start Disk Cleanup
    Cleanmgr
 3. To check drive letter while booting through bootable media
    diskpart
    list vol
 4. To Create install.wim file
    dism /capture-image /imagefile:E:\install.wim /capturedir:C:\ /ScratchDir:E:\Scratch /name:"WIN11x64-Jan22" /compress:maximum /checkintegrity /verify /bootable
 5. Download - Windows Assessment and Deployment Kit - https://learn.microsoft.com/en-us/windows-hardware/get-started/adk-install 
 6. To Create Bootable ISO
    oscdimg.exe -m -o -u2 -udfver102 -bootdata:2#p0,e,be:\my_files\boot\etfsboot.com#pEF,e,be:\my_files\efi\microsoft\boot\efisys.bin e:\my_files e:\WIN11x64-Jan22.iso
