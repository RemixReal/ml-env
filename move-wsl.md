# Moving a WSL distribution to another drive.

Comes in handy once disk space starts evaporating as you do ML work on WSL.

Thanks to: https://dev.to/mefaba/installing-wsl-on-another-drive-in-windows-5c4a

List the distributions and see which are running:

wsl --list -v

Terminate the distribution you want to move. In this example it's Ubuntu.

wsl -t "Ubuntu"

Export (backup) the distribution to a tar file somewhere.

wsl --export "Ubuntu" "D:\wsl_export\ubuntu-ex.tar"

Unregister previous WSL installation.

wsl --unregister "Ubuntu"

Use import to untar and register the distribution at the new location. 

wsl --import "Ubuntu" "D:\wsl\dist\ubuntu" "D:\wsl_export\ubuntu-ex.tar"

