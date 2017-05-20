# set-resolution
This is a simple Bash script that helps to change resolutions in linux systems.

Features are:
- Modeline adding on the fly
- Configurable labels for easy use

# Examples

    set-resolution VGA2 300x300
    set-resolution Virtual7 300x300
    set-resolution 1280x700  # uses the first connected output

You could practically use any silly resolution. Useful for virtual machines.

# Labels

Labels are configured in ~/.resolution-labels like this

    beamer 1280x720
    laptop 1980x1050
    
So just label, space, resolution, newline :)

You may now also call

    set-resolution beamer
    set-resolution laptop

    set-resolution Virtual3 laptop
    
and it'll use the configured resolution.

# Internal stuff and dependancies

It uses xrandr to change the resolution. If the resolution is not being found, its modeline is generated using cvt, added using xrandr, and then selected.

Therefore xrandr needs to be installed. 

Tested with xrandr 1.4.
