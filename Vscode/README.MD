# Visual Studio Code 

## Debian and Ubuntu based distributions

The easiest way to install Visual Studio Code for Debian/Ubuntu based distributions is to download and install the .deb package (64-bit), either through the graphical software center if it's available, or through the command line with:

```
sudo apt install ./<file>.deb
```

If you're on an older Linux distribution, you will need to run this instead:
``` 
sudo dpkg -i <file>.deb
sudo apt-get install -f # Install dependencies
```

### Other method
Installing the .deb package will automatically install the apt repository and signing key to enable auto-updating using the system's package manager. Note that other binaries are also available on the [VS Code download page](https://code.visualstudio.com/Download).

The repository and key can also be installed manually with the following script:
```
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```

Then update the package cache and install the package using:
```
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install code # or code-insiders
```

## Windows  

**Installation**

    1. Download the Visual Studio Code installer for Windows.
    2. Once it is downloaded, run the installer (VSCodeUserSetup-{version}.exe). This will only take a minute.
    3. By default, VS Code is installed under C:\users\{username}\AppData\Local\Programs\Microsoft VS Code.

Alternatively, you can also download a [Zip archive](https://code.visualstudio.com/docs/?dv=winzip), extract it and run Code from there.

   > **Note**: .NET Framework 4.5.2 or higher is required for VS Code. If you are using Windows 7, make sure you have at least .NET Framework 4.5.2 installed. You can check your version of [.NET Framework](https://www.microsoft.com/download/details.aspx?id=42643) using this command, reg query "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\full" /v version from a command prompt.
    
   > **Tip**: Setup will add Visual Studio Code to your %PATH%, so from the console you can type 'code .' to open VS Code on that folder. You will need to restart your console after the installation for the change to the %PATH% environmental variable to take effect.

