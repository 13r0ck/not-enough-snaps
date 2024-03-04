# Wezterm

## Build and install
```bash
# install snap
snapcraft && sudo snap install wezterm_*.snap --dangerous
sudo snap connect wezterm:network ssh-keys

# Seems not possible for a snap to be able to launch other snaps?
# Hack for now is just to ssh back into the machine ヽ༼ຈل͜ຈ༽ﾉ
# This assumes Ubuntu, otherwise replace ufw commands
sudo apt install openssh-server -y
sudo ufw enable
sudo ufw allow in from 127.0.0.1 to any port 22 proto tcp
ssh-copy-id $USER@localhost
# IMPORTANT!
# Now set the the terminal hotkey to run 'wezterm ssh <your username>@localhost'
# For example in gnome:
#	1. Settings -> Keyboard -> Keyboard Shortcuts
#	2. Disable the 'Launch Terminal' Shortcut
#	3. Create a custom shortcut <Ctrl>+<Alt>+t and assign to 'wezterm ssh <your username>@localhost'
```
