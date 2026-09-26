TetherFTP
=========

Extract the entire TetherFTP folder to a writable location and run TetherFTP.exe.
Keep the _internal folder beside the executable; it contains required runtime files.

Use File > New Session to manage connections and open SFTP or SSH tabs.
Help > Documentation contains a quick-start guide.

Saved connections live only in config/config.json beside the executable.
Passwords are encrypted with Windows DPAPI for the Windows account and computer
that saved them. No master password or separate key file is required.
To move connections to another account/computer, export without passwords and
re-enter the passwords there.

To clear saved connections, CLOSE TetherFTP, delete config/config.json or the
whole config folder, then reopen the app. The connection list will be empty.
There is no automatic restore from another folder or from an export file.

When updating, replace the executable and the entire _internal folder together.
Keep your config folder. Do not merge old and new runtime folders.

Brought to life by Pavan Jillela
