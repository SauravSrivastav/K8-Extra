# Step 1: Check Configurations:

> My PC -> Properties (Control Panel\System and Security\System)
> Later release of Windows 10
> Type "Winver" > Recommended is 2004 atleast > Windows update Settings 
> Turn Windows Features On and Off > Do not Enable "Windows Hypervisor Platform" > Enable Virtual Machine Platform and Windows Subsystem For Linux. 
> Restart Computer
> Go to Windows Store -> Search Ubuntu -> Install
> Output : 
# Installing, this may take a few minutes...Please create a default UNIX user account. The username does not need to match your Windows username.For more information visit: https://aka.ms/wslusers.Enter new UNIX username: #
> If you are getting error then -> This requires a Linux Kernel 
 Download the Linux kernel update package: https://docs.microsoft.com/en-us/windows/wsl/wsl2-kernel
 > Check Some Linux Commands: ls, pwd etc.
 > Open Powershell :
  # Check Version:   wsl -l -v
  # Set Version:     wsl --set-version Ubuntu-20.04
  #                  uname -a
                    lsb_release -a
                    wsl --shutdown
                    
