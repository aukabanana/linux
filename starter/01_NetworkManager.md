- `nmcli device wifi list`
- `nmcli device wifi connect <wifi-name> password <password>`
- `nmcli systemctl enable --now NetworkManager`
- `nmcli connection show --active`
- `nmcli device status`

### Reset signals wifi && connect again

- `nmcli radio wifi off && nmcli radio wifi on`
- `nmcli device wifi rescan`
- `nmcli device wifi connect <SSID> password <password>`

### Disconnect

- `nmcli connection down <SSID>`

### Connect again

- `nmcli connection up <SSID>`
