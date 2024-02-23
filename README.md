# Ansible-Role: acr-ansible-mate-customization

AIT-CyberRange: Customizes ubuntu mate desktop environment.


## Requirements

- Debian or Ubuntu 

## Role Variables

**Example config:**

```yaml
client_launcher_objects: 
  caja-filebrowser:
    launcher-location: /usr/share/applications/caja.desktop
    position: 10
  thunderbird:
    launcher-location: /usr/share/applications/thunderbird.desktop
    position: 20
  firefox:
    launcher-location: /usr/share/applications/firefox.desktop
    position: 30

client_additional_applications:
  - curl
  - python3

client_desktop_bg_src: files/wallpaper.png

client_files_src: files/desktop_files/
client_files_dest: /tmp/

```

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - cr-mate-customization
      vars:
        client_additional_applications:
          - curl
          - python3
```

## License

GPL-3.0

## Author

- Lenhard Reuter