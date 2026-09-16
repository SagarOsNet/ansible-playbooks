- unlike srv1, windows srv simply doesn't have pkg install cmd like "apt install apache"

So i tried a pkg manager for windows "chocolatey" more like apt bt for win software.

- However the pita was its apache pkg relies on another pkg (vcredist140) whose download link was dead.

- many automated attempts over WinRM to download apache got failed

*back to back time outs just for 14.5 mb apache zip file.

*I had no choice bt to manually download the zip via a browser on win srv itself, frm apachelounge.com (Win64 VS18 build)

- then i let my playbook extract + install it.

- also needed Microsoft's Visual C++ redistributable installed manually. Cause without it, Apache's program (httpd.exe) fails to even strt, with no error msg shown.
