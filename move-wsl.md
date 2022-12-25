# Moving a WSL distribution to another drive.

## References

This was partly informed by this helpful article - https://dev.to/mefaba/installing-wsl-on-another-drive-in-windows-5c4a

## Instructions

List the distributions on the local machine and see which are running:

    wsl --list -v

Terminate the distribution you want to move. In this example it's Ubuntu.

    wsl -t "Ubuntu"

Export (backup) the distribution to a tar file somewhere.

    wsl --export "Ubuntu" "D:\wsl_export\ubuntu-ex.tar"

Unregister previous WSL installation.

    wsl --unregister "Ubuntu"

Use import to untar and register the distribution at the new location. 

    wsl --import "Ubuntu" "D:\wsl\dist\ubuntu" "D:\wsl_export\ubuntu-ex.tar"

At this point, if you start the instance, **it will log you in as root** because the settings are not carried over when you move a distribution this way.  To fix that:

    ubuntu.exe config --default-user {your_default_user_name}

To get a sense of how this .exe is named for other distributions, here is the command for Ubuntu-20.04:

    ubuntu2004.exe config --default-user {your_default_user_name}

