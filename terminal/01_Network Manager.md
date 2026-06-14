nmcli device wifi list
nmcli device wifi connect <wifi-name> password <password>
nmcli systemctl enable --now NetworkManager
nmcli connection show --active
nmcli device status
