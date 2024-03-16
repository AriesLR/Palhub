![Aetherium Banner](https://raw.githubusercontent.com/AriesLR/Aetherium/main/docs/images/bannerlogo-alt.png)

# 

 #### Aetherium is your ultimate destination for streamlined game server management. Whether you're setting up a cozy gaming haven for friends on your local machine or harnessing the power of a Virtual Private Server (VPS), Aetherium empowers you every step of the way. Wave goodbye to clunky 'Start.bat' scripts and embrace the future of gaming with Aetherium at your side. Seamlessly launch, monitor, and maintain your game servers with ease.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Features](#features)
- [Planned Features](#planned-features)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Acknowledgements](#acknowledgements)
- [License](#license)
- [Tips](#tips)
- [Notes](#notes)

## Prerequisites

- Windows Notifications need to be turned on for warning/error/save messages, don't worry notifications from the app are silent. 

 > [!NOTE]  
> No manual installation is required for any prerequisites. If they're missing, Aetherium will prompt you to download them. Based on my testing, both components will likely be necessary for Windows Server systems. For regular Windows systems, [WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer/?form=MA13LH) should already be installed, but you may receive a prompt to install [.NET 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-8.0.201-windows-x64-installer).

## Features

- Start and stop server.
- Monitor server output in real-time.
- Automatic server restarts.
- Automatic save backups.
- RCON integration.
- Resource monitoring.
- Config profiles.

## Planned Features

- Light Theme (Currently dark by default)
- Multi-Server Support (Currently only supports 1 active server process)
- UI Overhaul

## Getting Started

To begin using Aetherium, you have the option to choose between an installer or a portable version. Follow the instructions below based on your preference:

### Installer Version:

1. **Download and Install**: Download `Aetherium-Setup.exe` from the [Releases](https://github.com/arieslr/Aetherium/releases/latest) page. Run the installer and follow the on-screen instructions to complete the installation process.

2. **Configure Your Server**: After installation, launch Aetherium and navigate to the configuration page to set up your server settings (see [Configuration](#configuration)).

3. **Start Your Server**: Once configured, start your server with a simple click and monitor its output in real-time.

### Portable Version:

1. **Download and Extract**: Download `Aetherium-Portable.zip` from the [Releases](https://github.com/arieslr/Aetherium/releases/latest) page. Extract the contents of the downloaded ZIP file to a folder of your choice on your machine.

2. **Run Aetherium**: Navigate to the extracted Aetherium folder and run the Aetherium executable (Aetherium.exe) to launch the application.

3. **Configure Your Server**: Upon launching, access the configuration page within Aetherium to set up your server settings (see [Configuration](#configuration)).

4. **Start Your Server**: Once configured, start your server effortlessly with a click of a button and monitor its output in real-time.


## Configuration

As Aetherium strives for universality, it offers a broader range of configuration options compared to similar applications. This comprehensive approach ensures adaptability across various game servers and environments. To assist users in setting up their servers, we're continually testing compatibility with additional games and providing example configurations below. While Aetherium aims to cover all essential settings, please consult the game's documentation for any specific configurations, especially if direct editing of the game server's configuration files is necessary.

### Config Help
|Section | Option | Input Type | Example |
| :---: | :---: | :---: | :---: |
| *File Paths* | Server Path | EXE | `C:\PalworldServer\Pal\Binaries\Win64\PalServer-Win64-Test-Cmd.exe` |
| *File Paths* | Save Path | Folder | `C:\PalworldServer\Pal\Saved\SaveGames\0` |
| *File Paths* | Backup Path | Folder | `C:\PalworldServerBackups` |
| *Parameters* | Launch Parameters | Game Specific | `-publiclobby -publicport=8211 -RCONPort=25575` |
| *Rcon* | IP | Server IP | `37.27.179.166` |
| *Rcon* | Port | Rcon Port, Game Specific | `25575` |
| *Rcon* | Password | Password, Game Specific | `SuperSecurePassword123` |
| *Intervals* | Backup Interval (Minutes) | Time, in minutes | `30` | 
| *Intervals* | Restart Interval (Minutes) | Time, in minutes | `180` |
###### That's a random IP, no need to worry thinking I intentionally put my own IP there.

### Example Configs

#### Palworld
![Palworld Config](https://raw.githubusercontent.com/AriesLR/Aetherium/main/docs/images/config/palworldconfig.png)

#### Arma 3
![Arma 3 Config](https://raw.githubusercontent.com/AriesLR/Aetherium/main/docs/images/config/arma3config.png)

#### Enshrouded
![Enshrouded Config](https://raw.githubusercontent.com/AriesLR/Aetherium/main/docs/images/config/enshroudedconfig.png)

## Acknowledgements
- [CoreRCON](https://github.com/Challengermode/CoreRcon) - For the .NET Standard implementation of the Source RCON Protocol.

- [Darkbyte](https://github.com/darkbyte42) - For all the input they've given so far, their suggestions are giving me direction on what features to add.

## License

[MIT License](LICENSE)

## Tips
[Buy Me a Coffee](https://www.buymeacoffee.com/arieslr)

## Notes

###### Firstly, this is my first windows application ever. I have web development experience as well as various other programming experience, but this has been a learning journey for me.

###### ~~This was created as a .NET Maui Blazor Hyrbid App. While .NET Maui seems to be a pretty capable framework, it has some limits. ~~

###### ~~My main example being an issue I encountered trying to use the windows file picker for the config setup. While I could get it to work partially, I found that it's likely impossible to get the full file path since .NET Maui Blazor Hybrids are technically web apps and for security reasons a browser can't get that kind of detailed information about a users file structure.~~

###### ~~While that's unfortunate and a slight inconvenience to the end-user I don't want to let something so small hold me back. I will continue to update and make this app as versatile as I can.~~

###### Using C# I was able to get the file picker working.

###### Fun Fact: Aetherium's original name was Palhub. When I originally started this project it was really just me learning and trying to create a server launcher for Palworld to replace the batch script I wrote. 
