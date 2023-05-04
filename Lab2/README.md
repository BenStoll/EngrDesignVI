# Lab 2 - Command Line
## I will be going through the commands and show exactly what they do on my machine.

```
$ hostname
$ env
$ ps
$ pwd
$ git clone https://github.com/kevinwlu/iot.git
$ cd iot
$ ls
$ cd
$ df
$ mkdir demo
$ cd demo
$ nano file
$ cat file
$ cp file file1
$ mv file file2
$ rm file2
$ clear
$ man uname
$ uname -a
$ ifconfig
$ ping localhost
$ netstat
```

### Results of Commands

```
$ hostname
DESKTOP-3U81CMS
```
The above command is used to display what the name of the host machine is.

```
$ env
USERDOMAIN=DESKTOP-3U81CMS
OS=Windows_NT
COMMONPROGRAMFILES=C:\Program Files\Common Files
SW_SIM_TEMP=C:\ProgramData\SOLIDWORKS\SW_net_sim_temp\
PROCESSOR_LEVEL=6
PSModulePath=%ProgramFiles%\WindowsPowerShell\Modules;C:\WINDOWS\system32\WindowsPowerShell\v1.0\Modules;C:\Program Files (x86)\Microsoft SQL Server\120\Tools\PowerShell\Modules\
CommonProgramW6432=C:\Program Files\Common Files
OPENCV_DIR=C:\Users\stoll\Desktop\opencv\build\x64\vc15
CommonProgramFiles(x86)=C:\Program Files (x86)\Common Files
LANG=en_US.UTF-8
MSYSTEM_CARCH=x86_64
DISPLAY=needs-to-be-defined
HOSTNAME=DESKTOP-3U81CMS
PUBLIC=C:\Users\Public
SW_SIM_HYDRA=C:\Program Files\Common Files\SolidWorks Shared\Simulation Worker Agent\
CONFIG_SITE=/mingw64/etc/config.site
EXEPATH=C:\Users\stoll\Vivado\2022.2\tps\win64\git-2.16.2
MSYSTEM_CHOST=x86_64-w64-mingw32
USERNAME=stoll
ChocolateyInstall=C:\ProgramData\chocolatey
LOGONSERVER=\\DESKTOP-3U81CMS
PROCESSOR_ARCHITECTURE=AMD64
ERLANG_HOME=C:\Program Files\erl9.2
LOCALAPPDATA=C:\Users\stoll\AppData\Local
COMPUTERNAME=DESKTOP-3U81CMS
FPS_BROWSER_APP_PROFILE_STRING=Internet Explorer
!::=::\
SYSTEMDRIVE=C:
USERPROFILE=C:\Users\stoll
PATHEXT=.COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC;.PY;.PYW
SYSTEMROOT=C:\WINDOWS
USERDOMAIN_ROAMINGPROFILE=DESKTOP-3U81CMS
PROCESSOR_IDENTIFIER=Intel64 Family 6 Model 142 Stepping 12, GenuineIntel
MINGW_PACKAGE_PREFIX=mingw-w64-x86_64
OneDriveConsumer=C:\Users\stoll\OneDrive
PWD=/c/WINDOWS/system32
SSH_ASKPASS=/mingw64/libexec/git-core/git-gui--askpass
HOME=/c/Users/stoll
TMP=/tmp
MSYSTEM_PREFIX=/mingw64
OneDrive=C:\Users\stoll\OneDrive
SW_SIM_MPIT=INTELMPI
RABBITMQ_NODENAME=rabbit@localhost
PROCESSOR_REVISION=8e0c
FPS_BROWSER_USER_PROFILE_STRING=Default
TMPDIR=/tmp
NUMBER_OF_PROCESSORS=8
ProgramW6432=C:\Program Files
COMSPEC=C:\WINDOWS\system32\cmd.exe
APPDATA=C:\Users\stoll\AppData\Roaming
SHELL=/usr/bin/bash
TERM=xterm
VXIPNPPATH=C:\Program Files (x86)\IVI Foundation\VISA\
WINDIR=C:\WINDOWS
MINGW_CHOST=x86_64-w64-mingw32
ProgramData=C:\ProgramData
SHLVL=1
PLINK_PROTOCOL=ssh
ACLOCAL_PATH=/mingw64/share/aclocal:/usr/share/aclocal
PROGRAMFILES=C:\Program Files
MANPATH=/mingw64/share/man:/usr/local/man:/usr/share/man:/usr/man:/share/man
ORIGINAL_TEMP=/tmp
ORIGINAL_TMP=/tmp
ALLUSERSPROFILE=C:\ProgramData
TEMP=/tmp
DriverData=C:\Windows\System32\Drivers\DriverData
MSYSTEM=MINGW64
MINGW_PREFIX=/mingw64
VXIPNPPATH64=C:\Program Files\IVI Foundation\VISA\
ProgramFiles(x86)=C:\Program Files (x86)
PATH=/c/Users/stoll/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:/c/Users/stoll/bin:/c/Python311/Scripts:/c/Python311:/c/Program Files (x86)/NVIDIA Corporation/PhysX/Common:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/Program Files (x86)/Windows Kits/8.1/Windows Performance Toolkit:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/110/Tools/Binn:/c/Program Files (x86)/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/DTS/Binn:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/Program Files/IVI Foundation/VISA/Win64/Bin:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/Program Files/PuTTY:/c/Program Files/MATLAB/R2022b/bin:/c/eda/ghdl:/c/eda/gtkwave:/c/Users/stoll/Desktop/opencv/build/bin:/c/Program Files/nodejs:/c/ProgramData/chocolatey/bin:/c/eda/GHDL/0.37-mingw32-mcode/lib/ghdl:/c/Users/stoll/Desktop/opencv/build/x64/vc15/bin:/c/Users/stoll/AppData/Local/Microsoft/WindowsApps:/c/Users/stoll/AppData/Local/atom/bin:/c/Users/stoll/AppData/Local/Programs/Microsoft VS Code/bin:/c/Users/stoll/AppData/Local/Microsoft/WindowsApps:/c/Users/stoll/Documents/Python - Exercism:/c/msys64/mingw64/bin:/c/msys64/usr/bin:/c/Users/stoll/AppData/Local/Programs/MiKTeX/miktex/bin/x64:/c/Users/stoll/MikTeX/miktex/bin/x64:/c/Users/stoll/AppData/Roaming/npm:/usr/bin/vendor_perl:/usr/bin/core_perl
PS1=\[\033]0;$TITLEPREFIX:$PWD\007\]\n\[\033[32m\]\u@\h \[\033[35m\]$MSYSTEM \[\033[33m\]\w\[\033[36m\]`__git_ps1`\[\033[0m\]\n$
HOMEDRIVE=C:
ChocolateyLastPathUpdate=133225899752863328
PKG_CONFIG_PATH=/mingw64/lib/pkgconfig:/mingw64/share/pkgconfig
INFOPATH=/usr/local/info:/usr/share/info:/usr/info:/share/info
HOMEPATH=\Users\stoll
ORIGINAL_PATH=/mingw64/bin:/usr/bin:/c/Users/stoll/bin:/c/Python311/Scripts:/c/Python311:/c/Program Files (x86)/NVIDIA Corporation/PhysX/Common:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/Program Files (x86)/Windows Kits/8.1/Windows Performance Toolkit:/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/110/Tools/Binn:/c/Program Files (x86)/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/Tools/Binn:/c/Program Files/Microsoft SQL Server/120/DTS/Binn:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/Program Files/IVI Foundation/VISA/Win64/Bin:/c/Program Files (x86)/IVI Foundation/VISA/WinNT/Bin:/c/Program Files/PuTTY:/c/Program Files/MATLAB/R2022b/bin:/c/eda/ghdl:/c/eda/gtkwave:/c/Users/stoll/Desktop/opencv/build/bin:/c/Program Files/nodejs:/c/ProgramData/chocolatey/bin:/c/eda/GHDL/0.37-mingw32-mcode/lib/ghdl:/c/Users/stoll/Desktop/opencv/build/x64/vc15/bin:/c/Users/stoll/AppData/Local/Microsoft/WindowsApps:/c/Users/stoll/AppData/Local/atom/bin:/c/Users/stoll/AppData/Local/Programs/Microsoft VS Code/bin:/c/Users/stoll/AppData/Local/Microsoft/WindowsApps:/c/Users/stoll/Documents/Python - Exercism:/c/msys64/mingw64/bin:/c/msys64/usr/bin:/c/Users/stoll/AppData/Local/Programs/MiKTeX/miktex/bin/x64:/c/Users/stoll/MikTeX/miktex/bin/x64:/c/Users/stoll/AppData/Roaming/npm
_=/usr/bin/env
```
The above command displays all environment variables on a machine
```
$ ps
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
    10580   14248   10580      13256  pty0      197609 15:06:16 /usr/bin/bash
    12852   10580   12852      14220  pty0      197609 15:10:20 /usr/bin/ps
    14248       1   14248      14248  ?         197609 15:06:16 /usr/bin/mintty
```
This command shows the active processes on the computer

```
stoll@DESKTOP-3U81CMS MINGW64 /c/WINDOWS/system32
$ pwd
/c/WINDOWS/system32
```
The above command shows the path to the current directory from the root directory.
```
PS C:\Users\stoll> git clone https://github.com/kevinwlu/iot.git
Cloning into 'iot'...
remote: Enumerating objects: 19225, done.
remote: Counting objects: 100% (274/274), done.
remote: Compressing objects: 100% (139/139), done.
remote: Total 19225 (delta 135), reused 186 (delta 93), pack-reused 18951
Receiving objects: 100% (19225/19225), 27.71 MiB | 5.60 MiB/s, done.
Resolving deltas: 100% (12834/12834), done.
Updating files: 100% (393/393), done.
PS C:\Users\stoll> cd iot
PS C:\Users\stoll\iot> ls


    Directory: C:\Users\stoll\iot


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----          5/4/2023   3:16 PM                .git
d-----          5/4/2023   3:16 PM                apps
d-----          5/4/2023   3:16 PM                cases
d-----          5/4/2023   3:16 PM                economics
d-----          5/4/2023   3:16 PM                health
d-----          5/4/2023   3:16 PM                hype
d-----          5/4/2023   3:16 PM                lesson1
d-----          5/4/2023   3:16 PM                lesson10
d-----          5/4/2023   3:16 PM                lesson2
d-----          5/4/2023   3:16 PM                lesson3
d-----          5/4/2023   3:16 PM                lesson4
d-----          5/4/2023   3:16 PM                lesson5
d-----          5/4/2023   3:16 PM                lesson6
d-----          5/4/2023   3:16 PM                lesson7
d-----          5/4/2023   3:16 PM                lesson8
d-----          5/4/2023   3:16 PM                lesson9
d-----          5/4/2023   3:16 PM                make
d-----          5/4/2023   3:16 PM                projects
d-----          5/4/2023   3:16 PM                special_pro
                                                  blems
d-----          5/4/2023   3:16 PM                standards
d-----          5/4/2023   3:16 PM                systems
d-----          5/4/2023   3:16 PM                tools
-a----          5/4/2023   3:16 PM          14329 README.md

PS C:\Users\stoll\iot>
```
The above code fragments clone Kevin Lu's respository and then navigates into the iot folder and lists what files are within that folder.

```
stoll@DESKTOP-3U81CMS MINGW64 /c/WINDOWS/system32
$ df
Filesystem                                        1K-blocks      Used Available Use% Mounted on
C:/Users/stoll/Vivado/2022.2/tps/win64/git-2.16.2 483902460 335082932 148819528  70% /
```
This is used to display the amount of free space on the computer.

```
PS C:\Users\stoll> cd demo
PS C:\Users\stoll\demo> nano file
PS C:\Users\stoll\demo> cat file
Hello everyone on the interwebs. I am a very hungery
spider and I am coming to eat you data
PS C:\Users\stoll\demo> cp file file1
PS C:\Users\stoll\demo> mv file file2
PS C:\Users\stoll\demo> rm file2
```
![image](https://user-images.githubusercontent.com/98097869/236307691-9af320b5-a350-4a17-8edc-fb818d11ccc6.png)

The above segments will create a file with name file and then we can add some text to the file. After saving the file, we use the cat command to read the file and then we copy the file (cp) and changes the name of file1 to file2. After that, we removed file2.

```
clear
```
Clear erases all the command prompts and outputs in the terminal.

```
PS C:\Users\stoll\demo> man uname
Get-Help : Get-Help could not find uname in a help file in
this session. To download updated help topics type:             "Update-Help". To get help online, search for the help topic    in the TechNet library at                                       https:/go.microsoft.com/fwlink/?LinkID=107116.                  At line:55 char:5                                               +     Get-Help @PSBoundParameters | more
+     ~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ResourceUnavailable: (:) [Get-He
   lp], HelpNotFoundException
    + FullyQualifiedErrorId : HelpNotFound,Microsoft.PowerShel
   l.Commands.GetHelpCommand
```
The man uname function is searching for a command of name uname and it doesn't exist in this directory. 

```
PS C:\Users\stoll> uname -a
MSYS_NT-10.0-22621 DESKTOP-3U81CMS 3.3.3-341.x86_64 2022-01-18 13:00 UTC x86_64 Msys
```
This command prints the kernel name, the network node hostname, the kernel release date, the kernel version, the machine hardware name, the hardware platform, and the operating system.

```
PS C:\Users\stoll> ipconfig

Windows IP Configuration


Wireless LAN adapter Local Area Connection* 1:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 2:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . : campus.stevens-tech.edu
   Link-local IPv6 Address . . . . . : fe80::e2ca:402b:eee7:d958%12
   IPv4 Address. . . . . . . . . . . : 10.156.128.220
   Subnet Mask . . . . . . . . . . . : 255.255.224.0
   Default Gateway . . . . . . . . . : 10.156.128.1

Ethernet adapter Bluetooth Network Connection:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :
```
I initially tried to use $ ifconfig, however it threw an error. I looked it up and found the ifconfig was deprecated and that I should use $ ipconfig instead and that is what gave the above result.

```
PS C:\Users\stoll> ping localhost

Pinging DESKTOP-3U81CMS [::1] with 32 bytes of data:
Reply from ::1: time<1ms
Reply from ::1: time<1ms
Reply from ::1: time<1ms
Reply from ::1: time<1ms

Ping statistics for ::1:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 0ms, Maximum = 0ms, Average = 0ms
```
This command pings the local host as a test and sends a few packets to test the connection and returns the statisitics for the test.
```
PS C:\Users\stoll> netstat

Active Connections

  Proto  Local Address          Foreign Address        State
  TCP    10.156.128.220:49445   52.159.127.243:https   ESTABLISHED
  TCP    10.156.128.220:52489   52.159.127.243:https   ESTABLISHED
  TCP    10.156.128.220:52534   ec2-35-169-123-237:https  ESTABLISHED
  TCP    10.156.128.220:52537   ec2-35-169-123-237:https  ESTABLISHED
  TCP    10.156.128.220:52538   ec2-35-169-123-237:https  ESTABLISHED
  TCP    10.156.128.220:52539   ec2-35-169-123-237:https  ESTABLISHED
  TCP    10.156.128.220:52540   ec2-35-169-123-237:https  ESTABLISHED
  TCP    10.156.128.220:52657   bl-in-f188:5228        ESTABLISHED
  TCP    10.156.128.220:52658   bl-in-f188:5228        ESTABLISHED
  TCP    10.156.128.220:53404   62:https               TIME_WAIT  TCP    10.156.128.220:53769   104.36.115.111:https   ESTABLISHED
  TCP    10.156.128.220:53966   ec2-52-4-55-187:https  ESTABLISHED
  TCP    10.156.128.220:54030   211:https              ESTABLISHED
  TCP    10.156.128.220:54122   ec2-54-159-61-126:https  ESTABLISHED
  TCP    10.156.128.220:54903   162.248.18.36:https    ESTABLISHED
  TCP    10.156.128.220:56589   172.64.192.18:https    ESTABLISHED
  TCP    10.156.128.220:56706   151.101.194.49:https   ESTABLISHED
  TCP    10.156.128.220:56707   151.101.193.44:https   ESTABLISHED
  TCP    10.156.128.220:56787   server-52-85-61-93:https  TIME_WAIT
  TCP    10.156.128.220:56858   ec2-3-89-1-23:https    ESTABLISHED
  TCP    10.156.128.220:56868   104.18.21.134:https    ESTABLISHED
  TCP    10.156.128.220:56881   wv-in-f154:https       TIME_WAIT  TCP    10.156.128.220:56886   mad41s07-in-f3:https   ESTABLISHED
  TCP    10.156.128.220:56889   lga25s72-in-f14:https  TIME_WAIT  TCP    10.156.128.220:56904   209.54.180.212:https   ESTABLISHED
  TCP    10.156.128.220:56905   209.54.180.212:https   TIME_WAIT  TCP    10.156.128.220:56906   209.54.180.212:https   TIME_WAIT  TCP    10.156.128.220:56919   a104-126-118-248:https  ESTABLISHED
  TCP    10.156.128.220:56922   lb-140-82-112-25-iad:https  ESTABLISHED
  TCP    10.156.128.220:56923   183:https              ESTABLISHED
  TCP    10.156.128.220:56965   8.43.72.24:https       ESTABLISHED
  TCP    10.156.128.220:56975   50.57.31.206:https     ESTABLISHED
  TCP    10.156.128.220:57008   lga34s33-in-f3:https   TIME_WAIT  TCP    10.156.128.220:57011   ec2-3-226-3-84:https   ESTABLISHED
  TCP    10.156.128.220:57077   52.114.128.83:https    ESTABLISHED
  TCP    10.156.128.220:57129   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57130   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57132   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57133   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57134   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57135   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57140   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57141   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57142   147.28.129.37:https    ESTABLISHED
  TCP    10.156.128.220:57143   8.2.111.196:https      ESTABLISHED
  TCP    10.156.128.220:57146   8.2.111.196:https      ESTABLISHED
  TCP    10.156.128.220:57147   8.2.111.196:https      ESTABLISHED
  TCP    10.156.128.220:57152   8.2.111.196:https      ESTABLISHED
  TCP    10.156.128.220:57153   8.2.111.196:https      ESTABLISHED
  TCP    10.156.128.220:57154   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57155   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57156   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57157   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57160   ip186:https            ESTABLISHED
  TCP    10.156.128.220:57165   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57166   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57174   72.251.238.254:https   ESTABLISHED
  TCP    10.156.128.220:57178   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57179   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57180   ec2-35-174-95-110:https  ESTABLISHED
  TCP    10.156.128.220:57181   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57182   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57183   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57184   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57185   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57186   155.246.1.20:domain    TIME_WAIT  TCP    10.156.128.220:57187   192.184.68.149:https   ESTABLISHED
  TCP    10.156.128.220:57188   ec2-52-6-111-222:https  ESTABLISHED
  TCP    10.156.128.220:57189   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57190   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57192   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57193   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57194   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57195   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57196   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57197   ec2-3-225-218-10:https  ESTABLISHED
  TCP    10.156.128.220:57198   ec2-44-205-45-11:https  ESTABLISHED
  TCP    10.156.128.220:57199   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57200   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57201   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57202   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57203   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57204   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57207   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57208   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57209   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57210   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57213   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57214   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57215   218:https              ESTABLISHED
  TCP    10.156.128.220:57216   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57217   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57218   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57219   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57220   ec2-34-225-3-139:https  ESTABLISHED
  TCP    10.156.128.220:57221   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57224   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57226   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57227   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57228   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57229   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57231   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57232   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57234   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57235   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57236   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57237   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57238   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57240   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57241   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57243   173:https              ESTABLISHED
  TCP    10.156.128.220:57244   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57245   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57246   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57247   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57248   li1886-22:https        ESTABLISHED
  TCP    10.156.128.220:57251   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57252   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57253   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57254   216.200.232.253:https  ESTABLISHED
  TCP    10.156.128.220:57255   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57256   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57257   104.18.23.234:https    ESTABLISHED
  TCP    10.156.128.220:57258   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57259   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57260   49:https               TIME_WAIT
  TCP    10.156.128.220:57261   a23-219-94-58:https    ESTABLISHED
  TCP    10.156.128.220:57262   nrac:domain            TIME_WAIT
  TCP    10.156.128.220:57263   172.67.8.174:https     ESTABLISHED
  TCP    10.156.128.220:57264   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57265   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57266   ec2-3-209-207-39:https  ESTABLISHED
  TCP    10.156.128.220:57267   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57268   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57270   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57275   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57276   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57277   201:https              ESTABLISHED
  TCP    10.156.128.220:57278   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57279   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57280   201:https              ESTABLISHED
  TCP    10.156.128.220:57281   69.166.1.14:https      ESTABLISHED
  TCP    10.156.128.220:57282   bidder:https           ESTABLISHED
  TCP    10.156.128.220:57283   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57284   155.246.1.20:domain    TIME_WAIT
  TCP    10.156.128.220:57285   69.166.1.14:https      ESTABLISHED
  TCP    10.156.128.220:57286   678:https              ESTABLISHED
  TCP    10.156.128.220:57287   e2:https               ESTABLISHED
  TCP    10.156.128.220:57289   155.246.1.20:domain    FIN_WAIT_1
  TCP    10.156.128.220:57290   155.246.1.20:domain    FIN_WAIT_1
  TCP    10.156.128.220:57485   8.43.72.97:https       TIME_WAIT
  TCP    10.156.128.220:57488   8.43.72.97:https       ESTABLISHED
  TCP    10.156.128.220:57565   lga34s38-in-f14:https  TIME_WAIT
  TCP    10.156.128.220:57583   lga25s79-in-f2:https   TIME_WAIT
  TCP    10.156.128.220:57596   151.101.1.229:https    ESTABLISHED
  TCP    10.156.128.220:57608   lga25s81-in-f2:https   TIME_WAIT
  TCP    10.156.128.220:57678   218:https              ESTABLISHED
  TCP    10.156.128.220:57679   104.22.68.131:https    ESTABLISHED
  TCP    10.156.128.220:57740   lga25s81-in-f2:https   TIME_WAIT
  TCP    10.156.128.220:57763   151.101.129.229:https  ESTABLISHED
  TCP    10.156.128.220:57766   lga25s79-in-f2:https   TIME_WAIT
  TCP    10.156.128.220:57799   lga25s81-in-f2:https   TIME_WAIT
  TCP    10.156.128.220:57800   lga25s71-in-f6:https   TIME_WAIT
  TCP    10.156.128.220:57807   49:https               ESTABLISHED
  TCP    10.156.128.220:57874   213:https              ESTABLISHED
  TCP    10.156.128.220:57898   8.43.72.98:https       TIME_WAIT
  TCP    10.156.128.220:57899   8.43.72.98:https       TIME_WAIT
  TCP    10.156.128.220:57919   8.43.72.98:https       TIME_WAIT
  TCP    10.156.128.220:57923   96.46.186.57:https     ESTABLISHED
  TCP    10.156.128.220:64609   ip-185-184-8-90:https  ESTABLISHED
  TCP    10.156.128.220:64629   maa03s26-in-f3:https   TIME_WAIT
  TCP    10.156.128.220:64682   bl-in-f156:https       TIME_WAIT
  TCP    10.156.128.220:64685   lga25s79-in-f4:https   TIME_WAIT
  TCP    10.156.128.220:64718   lga25s73-in-f2:https   TIME_WAIT
  TCP    10.156.128.220:64730   server-18-164-111-219:https  ESTABLISHED
  TCP    10.156.128.220:64780   104.26.7.139:https     ESTABLISHED
  TCP    10.156.128.220:64782   104.22.52.173:https    ESTABLISHED
  TCP    10.156.128.220:64785   104.22.53.86:https     ESTABLISHED
  TCP    10.156.128.220:64797   172.67.23.234:https    ESTABLISHED
  TCP    10.156.128.220:64802   172.67.69.19:https     ESTABLISHED
  TCP    10.156.128.220:64815   lga34s34-in-f1:https   TIME_WAIT
  TCP    10.156.128.220:64827   104.22.5.69:https      ESTABLISHED
  TCP    10.156.128.220:64834   104.36.115.123:https   ESTABLISHED
  TCP    10.156.128.220:64835   172.67.75.241:https    TIME_WAIT
  TCP    10.156.128.220:64873   139:https              ESTABLISHED
  TCP    10.156.128.220:64883   172.67.75.241:https    TIME_WAIT
  TCP    10.156.128.220:64902   104.22.5.69:https      ESTABLISHED
  TCP    10.156.128.220:64921   104.22.5.69:https      ESTABLISHED
  TCP    10.156.128.220:64937   ec2-184-72-144-54:https  ESTABLISHED
  TCP    10.156.128.220:64984   8.28.7.92:https        ESTABLISHED
  TCP    10.156.128.220:65019   168:https              ESTABLISHED
  TCP    10.156.128.220:65023   8.43.72.98:https       ESTABLISHED
```
This command shows the active connections on my computer.
