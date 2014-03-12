Linux SignTool bash script wrapper

Simple script wrapper for signing/resigning ZIP or APK files.

After downloading/cloning repository to desired folder run:

sign_zip install

After confirmation, path to sign_zip will be appended to your PATH
environment variable (user based) into your ~/.bashrc

after that you have 2 options to call it:

sign_zip package.zip

That will check package.zip for old signature files and remove it
and will sign file with test keys and signapk.jar file

Second option is:

sign_zip package.zip backup

That will do same thing, except it will create backup file
before any modifications where original file exists.

Backup file will have timestamp at beggining of filename, something like:
20140312135402_package.zip

Note:

Script depends on java and zip utility installed on host and
it makes checks for that. If java or zip is not found it will
report an error and exit.

In the end, I do not take any responsibility for usage in illegal
purposes or any harm done, bricked devices and so on :-)

Tool tested on Debian 7.4 x64, should work with all distros.
Feel free to PR, comment, open an issue...
