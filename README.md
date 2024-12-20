# Palword Dedicated Server

## Steps
---

Update your system:
```bash
sudo apt update && sudo apt upgrade -y
```

Install SteamCMD:
```bash
# Create the Steam user
sudo useradd -m -s /bin/bash steam

# Set a strong password
sudo passwd steam

# Install SteamCMD
sudo add-apt-repository multiverse; sudo dpkg --add-architecture i386; sudo apt update
sudo apt install steamcmd
```
>[!IMPORTANT]
>If you are using other distro visit: https://developer.valvesoftware.com/wiki/SteamCMD

Install the game as **steam** user
```bash
# 2GB+ will be needed on the steam's home directory
# If fails, run it again
# Check ~/.local/share/Steam
steamcmd +login anonymous +app_update 2394010 validate +quit
```
Server configuration
The configuration example and the default configurations can be found in  `/home/steam/.local/share/Steam/steamapps/common/PalServer/DefaultPalWorldSettings.ini`

>[!CAUTION]
>Do not make changes on DefaultPalWorldSettings.ini file and make a copy of it

```bash
# Copy de default configuration to PalWorldSettings.ini and make your customization
cp ~/.local/share/Steam/steamapps/common/PalServer/DefaultPalWorldSettings.ini ~/.local/share/Steam/steamapps/common/PalServer/Pal/Saved/Config/LinuxServer/PalWorldSettings.ini
```
