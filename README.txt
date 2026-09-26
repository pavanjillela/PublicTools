TetherFTP - Windows Installer
Version: 0.1.0
Installer: TetherFTP-Setup-0.1.0-x64.exe

ABOUT TETHERFTP
==============
TetherFTP is a Windows connection manager and SFTP client for managing
remote servers from one tabbed workspace. It combines a WinSCP-style
dual-pane file browser with an embedded SSH terminal, so you can transfer
files and run commands without switching between separate applications.

KEY FEATURES
============
- Browse local and remote folders side by side and transfer files by
  dragging and dropping them into the transfer queue.
- Open multiple remote sessions in tabs.
- Run remote commands in an embedded SSH terminal with copy, paste,
  keyboard shortcuts, and scrollback.
- Organize saved connections into folders in the Login / Site Manager.
- Manage reusable credentials for individual sites or entire folders.
- View remote file properties and change permissions when authorized.
- Switch remote users through sudo when the server permits it.
- Launch additional connection types through external applications,
  including PuTTY for SSH/Telnet, Windows Remote Desktop, and a browser.

REQUIREMENTS
============
- A Windows computer capable of running 64-bit x64 applications.
- Network access and valid credentials for the remote servers you use.
- SFTP/SSH support on the remote server for file transfers and terminals.
- Python and its dependencies do not need to be installed separately.
- External protocol tools, such as PuTTY or a VNC viewer, must be available
  separately if you use those connection types. PuTTY is not bundled.

INSTALLATION
============
1. Run TetherFTP-Setup-0.1.0-x64.exe.
2. Follow the setup wizard and choose the installation location.
3. Optionally select the desktop shortcut.
4. Finish setup and launch TetherFTP from the Start menu or shortcut.

Setup installs for the current Windows user. The default location is:
  %LOCALAPPDATA%\Programs\TetherFTP

Administrator access is not required for the default installation.
Choose a writable folder because TetherFTP stores its settings beside
the application.

FIRST CONNECTION
================
1. In the Login / Site Manager, select File > New Site.
2. Enter the server address, port, username, and authentication details.
   The usual SFTP/SSH port is 22 unless your server uses another port.
3. Select File > Save to save the site.
4. Select Login to open the SFTP file browser, or Open Shell to open
   an embedded terminal.
5. Use File > New Session to open additional connections.

Use Tools > Manage Credentials to create reusable logins.
Help > Documentation provides the built-in quick start.

CONFIGURATION AND SAVED CONNECTIONS
===================================
This installer does NOT include or copy any existing configuration,
saved connections, passwords, or exported connection lists.
A fresh installation starts with an empty connection list.

Settings created while using the application are stored at:
  <installation folder>\config\config.json

Saved passwords use Windows DPAPI encryption tied to the current Windows
account and computer. There is no separate master password. To transfer
sites to another account or computer, export without passwords and enter
the passwords again on the destination.

UPGRADING
=========
Close TetherFTP and run the new installer using the same installation
folder. Setup replaces the application runtime and preserves existing
user configuration. Existing saved connections are not reset by an upgrade.

UNINSTALLING
============
Use Windows Settings > Apps to uninstall TetherFTP.
User-created configuration is preserved. To remove it too, close the app
and delete the config folder inside the installation folder. Deleting
that folder permanently removes the settings and saved connections there.

NOTES
=====
- Remote access is limited by the permissions of your server account.
- Switch User requires suitable server-side sudo permissions; it does
  not bypass authentication or access controls.
- If a connection fails, check the server address, port, credentials,
  network/VPN access, and the server's SSH/SFTP availability.
