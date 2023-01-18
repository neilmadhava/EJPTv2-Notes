# Alternate Data Streams:

- File on NTFS formatted drive has 2 streams:
	- Data stream: default stream - contains data
	- Resource stream: used for metadata

- in cmd:
	- notepad test.txt:secret.txt
	- if some text is stored in secret.txt, it won't be visible in test.txt
	- type payload.exe > windowslog.txt:winpass.exe
	- mklink wsupdate.exe windowslog.txt:winpass.exe
	- wupdate