# Git

## Build and install
```bash
snapcraft && sudo snap install git_*.snap --dangerous
```

## Permissions
```bash
snap connect git:home
snap connect get:network
```

## Optional Permissions
```bash
# If cloning a repo via ssh
snap connect git:ssh-keys 

# If using Yubikey SSH authentication
snap connect git:raw-usb
snap connect git:removable-media
```
