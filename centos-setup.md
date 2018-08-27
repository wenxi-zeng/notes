# notes
# CentOS Setup

## Install CentOS with a flash drive
Remember to add the user to administrator group when create an user.

## Setup network

1. List ethernet card
    ```bash
    nmcli d
    ```

2. Open Network manager and edit connection.
    ```bash
    nmtui
    ```
    Choose “Automatic” in IPv4 CONFIGURATION and check Automatically connect check box and press OK and quit from Network manager.

3. Reset network service
    ```bash
    service network restart
    ```
    
## Setup UI (if CentOS minimal)

1. List available package groups
    ```bash
    yum group list
    ```
    
2. Install Gnome GUI packages
    ```bash
    yum groupinstall "GNOME Desktop" "Graphical Administration Tools"
    ```

3. Enable GUI on system startup
    ```bash
    ln -sf /lib/systemd/system/runlevel5.target /etc/systemd/system/default.target
    ```

4. Reboot the machine to start the server in the graphical mode
    ```bash
    reboot
    ```


## References
Setup network: https://lintut.com/how-to-setup-network-after-rhelcentos-7-minimal-installation/

Setup UI:https://www.itzgeek.com/how-tos/linux/centos-how-tos/install-gnome-gui-on-centos-7-rhel-7.html



