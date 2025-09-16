Load modules:
```bash
module load LUMI/24.03
module load systools    # provides Singularity/Apptainer
```



Build a writable development container

```bash
singularity build --sandbox webbrowsing.sif webbrowsing.def

singularity exec web_browsing.sif /bin/bash

lynx https://csc.fi/en/
```


Here the tools like lynx can show web pages as formatted text, but they cannot render images inside a pure terminal. At best, they’ll show [IMAGE] markers or ALT text.

If you are using a terminal emulator that supports inline graphics (e.g. Kitty, iTerm2 with imgcat, or wezterm), then some text-based browsers (w3m-img) can display inline images — but that requires extra support both in the browser and the terminal. On LUMI’s HPC environment, you normally just get a standard text-only terminal over SSH, so inline images aren’t possible.

For full graphical browsing (Firefox, Chromium, etc.), you’d need to run them under X11 forwarding, Wayland remote desktop, or through something like VNC/NoMachine — which is heavier and usually not what you want on login/compute nodes.

👉 For your current use case (secure sandboxed browsing with Lynx), expect only text-based interaction, no images.
