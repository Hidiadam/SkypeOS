# SkypeOS

***SkypeOS*** is an extremely lightweight *(~280 MB)* Porteus Kiosk based operating system that utilizes Google Chrome and the [Skype Web App](https://web.skype.com) to create an exceptionally easy-to-use, grandparent-friendly fullscreen environment for those who are afraid to use Windows.

After pressing the power button on the PC, Skype opens automatically without any user interaction required.

In the current SkypeOS configuration, access to every URL is blocked except the ones that are required for the usage of Skype and the login process. This configuration minimizes the risk of getting viruses, offering peace of mind for elderly users who may have concerns about security.

SkypeOS can be installed permanently to your computer's hard drive / SSD, or can be booted and used with full functionality from a pendrive or any bootable, read-write capable non-optical storage media.

## System requirements

 - This is an X86_64 bit based linux distribution, so your CPU has to be based on 64 bit architecture.
 - RAM: 1 GB
 - Storage*: 2 GB
 - Supports both UEFI and Legacy bios

Check the official [requirements here](https://porteus-kiosk.org/index.html#requirements) in detail.

\**(In my experience, 500MB of storage suffices.)*

## Installation

To install SkypeOS from the provided ISO, you will have to follow these steps:
1. Download the SkypeOS-[version_number].iso file. You can do that by clicking on the file name under Releases on the right of your screen, or by clicking [this](https://github.com/Hidiadam/SkypeOS/releases/download/v1.0/SkypeOS-1.0.iso) link.

2. Now you'll need a tool to flash the SkypeOS image onto your flash drive/hard drive.
	I recommend [balenaEtcher](https://etcher.balena.io), because it's free and provides a clean, beginner-friendly user interface. Alternatively, you can use Rufus or the *dd* utility if you're using linux.
	Using a flashing software is pretty straightforward; you’ll need to select the downloaded .iso, the target device, and then click ‘Flash!’.
	If you'd like to use a PC only for SkypeOS, you'll have to flash the provided ISO file *directly* to the main storage of the PC. Or you can execute a manual installation if you'd like to use an installer instead of directly flashing the premade ISO.

3. Boot the target PC from the flashed storage media. You can commonly select a bootable device by pressing the DEL or F12 key on your keyboard while you're starting up the computer.

4. Log into Skype and use it.

	Now, even after switching off the PC by pressing the power button and rebooting it, the user will remain logged into their Skype account. This is made possible through full persistence, ensuring that login activities are saved to the storage media. This eliminates the need for a keyboard on subsequent uses.

## Manually configured installation

In case you'd like to have full control over the configuration, follow these points:
1. Download the Porteus Kiosk installer from its [official site](https://porteus-kiosk.org/download.html), and create a bootable installation media.
2. Boot your PC from the flash drive, and select your preferred internet connection method.
3. Select Google Chrome as a browser *(Skype for web doesn’t work with its full functionality in Firefox.)*
4. Load the configuration file from *another* flash drive, or make your own config with the wizard. If you'd like to modify the configuration parameters manually, check the documentation for them [here](https://porteus-kiosk.org/parameters.html). Take a look at SkypeOS's [config settings](https://github.com/Hidiadam/SkypeOS/blob/main/SkypeOS-config.txt) for reference.
5. Select your storage, and install it.
Note that you won't have custom background with this solution.

## FAQ

1. *No sound / Webcam is not recognized*
   - Use manual installation, and select a default sound output and/or microphone input during the installation process.

4. *PC boots successfully, but Skype doesn't show up*
    - Check if you've correctly plugged in the Ethernet cable into your PC. For a wireless internet connection, you’ll have to perform a manual installation.
