# Break Reminder
This is a systemd timer that reminds you to take a break every 15 minutes. It uses `notify-send`.

# Install
Download the repository files into your systemd units folder, and then `systemctl enable` the timer:
```
mkdir -p ~/.local/share/systemd/user
curl https://raw.githubusercontent.com/leifmetcalf/break-reminder/master/break-reminder.service -o ~/.local/share/systemd/user/break-reminder.service
curl https://raw.githubusercontent.com/leifmetcalf/break-reminder/master/break-reminder.timer -o ~/.local/share/systemd/user/break-reminder.timer
systemctl --user enable --now break-reminder.timer
```
