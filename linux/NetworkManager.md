### Basic Connection

- `nmcli device wifi list`
- `nmcli device wifi connect <wifi-name> password <password>` or `nmcli --ask dev wifi connect <SSID>`
- `systemctl enable --now NetworkManager`
- `nmcli connection show --active`
- `nmcli device status`

### Reset signals wifi && connect again

- `nmcli radio wifi off && nmcli radio wifi on`
- `nmcli device wifi rescan`
- `nmcli device wifi connect <SSID> password <password>`

### Disconnect/Connect/Delete

- `nmcli connection down <SSID>`
- `nmcli connection up <SSID>`
- `nmcli connection delete <SSID>`

### Log

- `sudo journalctl -u NetworkManager -e -n 15`

-e : Pager end
-n 15 : Show only 15 lines