# set-resolution
This is a simple Bash script that helps to change resolutions in linux systems.

Features are:
- Modeline adding on the fly
- Configurable labels for easy use

# Examples

    set-resolution 1280x700
    set-resolution 300x300

You could practically use any silly resolution. Useful for virtual machines.

# Labels

Labels are configured in ~/.resolution-labels like this

    beamer 1280x720
    laptop 1980x1050
    
So just label, space, resolution, newline :)

You may now also call

    set-resolution beamer
    set-resolution laptop
    
an it will use the configured resolution behind the label.

# Internal stuff

It uses xrandr to change the resolution. If the resolution is not being found, its modeline is generated using cvt, added using xrandr again in order to be able to change it. So it's quite easy.
