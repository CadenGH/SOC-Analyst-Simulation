# SOC-Analyst-Simulation

  <h1>Description of this project until I manage to come around again and implement pictures and steps:</h1> 

  &nbsp;&nbsp;&nbsp;&nbsp;For my SOC Analyst Simulation I created and used 2 virtual machines using VMWare Workstation, one Ubuntu based Linux OS VM and one Windows OS VM. In this scenario the
  Linux machine was the attacker, while the Windows machine was the victim. 
	
  &nbsp;&nbsp;&nbsp;&nbsp;I configured the Windows VM to have worse than default security settings, and I downloaded and set up Sysmon, as my first SIEM tool for the project. I configured
  Sysmon with a preset config from an individual I found on a forum. I then configured my second SIEM tool LimaCharlie, a very powerful EDR. 

 &nbsp;&nbsp;&nbsp;&nbsp;As for the attacker’s machine (Linux VM) configurations, the first thing I did was set up Sliver.
 Which is often used by red teamers and penetration testers. 
 
 &nbsp;&nbsp;&nbsp;&nbsp;I launched Sliver and planted a Command and Control(C2) payload into my Windows VM. 
I was able to see my Sliver payload on my EDR(LimaCharlie). Which is cool, but I wanted to explore more. I went ahead and
dumped the LSASS process into a file. Not for any information / benefit, but it is  a real world scenario that can be used to
pull credentials from a computer. 
  
  &nbsp;&nbsp;&nbsp;&nbsp;I detected the lsass dump with LimaCharlie instantly, but I had to look for it. I know that
  analyzing strictly with eye-sight was nowhere near efficient or reliable. I
  read up on how to create alerts for specific flags, which I did for this project. I created an automatic alert for whenever
  the lsass process’ information is tampered with at all. 
	
  &nbsp;&nbsp;&nbsp;&nbsp;As of now, that’s most likely where I’m going to leave this project in terms of analysis and
  monitoring. I plan to explore a bit more on how I can use Sliver and other
  softwares to really dig into machines.
