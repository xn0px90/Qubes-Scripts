# qubes-scripts
Collection of custom scripts for Qubes OS

### Installation:
Just drop the scripts you want in `/usr/local/bin` on dom0 ([how to copy files to dom0](https://www.qubes-os.org/doc/how-to-copy-from-dom0/#copying-to-dom0))

### Explanation / Usage:
- `qubes-dom0-copy/move`: **import files to dom0 from other vms**; run the script, select the qube, then the files, and they will appear in the current directory on dom0 (and deleted on the source vm if moving)
- `qubes-flameshot`: **screenshot with flameshot and copy to qube clipboard**; run the script, make the screenshot, select target qube, paste to your heart's content
- `qubes-screenshare`: **quickly start a video companion screenshare session**; run the script, select destination qube, then source qube, do what you need, then stop screensharing with the tray icon
- `qubes-select-qube`: **show a prompt to select a qube**; intended for use in scripts and commands, all other scripts here rely on it

### Dependencies:
For the target qubes:

```bash
sudo dnf install \
    qubes-video-companion-receiver \
    xclip \
    yad
```

For dom0:
```bash
sudo qubes-dom0-update \
    flameshot \
    qubes-video-companion-dom0 \
    yad
```

### Disclaimer:
You should be careful what you do with dom0, I won't be held responsible if anything gets compromised. Make sure you understand exactly what these scripts are doing (they are in fact quite simple) before you run them.
