:warning: **Always** use source code from a [Release](https://github.com/HatchesPls/GrandTheftAutoV-Cheat/releases); the main branch might not contain stable code. See the Git information below for further instructions.

# Grand Theft Auto V Cheat
Regularly maintained free open-source internal cheat software for Grand Theft Auto V (PC). This project is originally based on the Nano42 (Sudomod) base but has over the years been significantly improved.

![](https://raw.githubusercontent.com/HatchesPls/GrandTheftAutoV-Cheat-Resources/367a55be9220d914a742341c045d001853e881c5/preview_image.png)

## Contents
* [Usage](#usage)
  * [Precompiled DLL](#download-precompiled-dll)
  * [Compile it yourself](#compile-it-yourself)
* [Updating](#updating)
* [Features](#features)

## Usage
### Using launcher (recommended)
The easiest way to get started is by using the Launcher, this program automatically downloads and injects the cheat. No need to separately download any other files or a injector.

Source code repository: https://github.com/HatchesPls/GrandTheftAutoV-Cheat-Launcher

[Direct download link](https://github.com/HatchesPls/GrandTheftAutoV-Cheat-Launcher/releases/download/v1.0/GTAVCheat_Launcher.exe)

### Download precompiled DLL
1. Download the latest compiled version (GTAV.dll) from the [Releases page](https://github.com/HatchesPls/GrandTheftAutoV-Cheat/releases)
2. Use your favorite injector to inject the cheat file into GTA5.exe. It is important to inject using the LoadLibrary method without any obfuscation or post injection cleanup, the cheat does **not** work when the cheat is manually mapped into the game process. If you don't know any module injectors, see [this](https://github.com/HatchesPls/SimpleModuleInjector) GitHub repository.
### Compile it yourself
1. Download and install [Git](https://git-scm.com/download/win) if you have not already.
2. Download and install [Microsoft Visual Studio (latest version)](https://visualstudio.microsoft.com/downloads/) if you have not already. Be sure to install the C++ packages when asked, these are required.
2. Open a Commmand Prompt (`cmd.exe`) window and navigate to (`cd`) the directory you wish to download the repository in (it will create a directory within this directory).
3. Run `git clone --recursive https://github.com/HatchesPls/GrandTheftAutoV-Cheat`

As the main branch is used for development we want to switch to the latest Release.

4. Run `git tag` (you might need to press Enter to see the whole list, press q to exit): this gives you a list of of all Releases.
5. Run `git checkout --recurse-submodules <version_number>` Replace <version_number> with the latest/higher version tag listed in the previous command

Example: `git checkout --recurse-submodules v2.2.2.0`

6. Navigate to the repository directory and open the GTAV.sln file.
7. Within VS, in the topmenu, go to Build -> Build GTAV or press Control + B.

Once compilation is completed, you will find a 'GTAV.dll' file in the Build directory of the Project.

## Updating
(when using the launcher, you will automatically always use the latest version)

A in-game message is shown whenever a newer version is available (assuming your system is connected to the internet). 

If you do not want to compile it yourself simply head to the [Releases section](https://github.com/HatchesPls/GrandTheftAutoV-Cheat/releases/latest) and download the latest DLL version from there.

To update your locally downloaded repository, follow below steps.
1. Open a Command Prompt (`cmd.exe`) within the repository directory.
2. Run `git pull --recurse-submodules`
3. Run `git checkout --recurse-submodules <version_number>` Replace <version_number> with whatever the latest version tag is.

From here on follow above steps to (re)compile the project within VS.

## Features
- In-game GUI 100% drawn using game functions and can be repositioned and controlled using mouse cursor
- Ability to save Selectable states (which are than auto loaded again at startup)
- Automatic update availability check (using Github API) and in-game notification
- Custom Textures (modifiable to your liking)
- Logger system including automatic cleanup
- Safe mode (ensures potentially 'unsafe' features are not available by default*)
- Script Events protection
- Storable custom teleport locations
- Theme Loader (ability to store UI component positions, change color and more)

and much more (coming)...

*See the [license](https://github.com/HatchesPls/GrandTheftAutoV-Cheat/blob/main/LICENSE) of this project for any unclarity on responsibility and liability on the software provided
