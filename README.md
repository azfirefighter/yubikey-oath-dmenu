yubikey-oath-dmenu
===

[dmenu][] interface for getting OATH codes from a [YubiKey][]

This program lets you pick an OATH credential from your YubiKey using [dmenu][],
and copies the corresponding OTP to the clipboard using [xclip][].
Alternatively, it can "type" the OTP using [xdotool][].

Notable features:

- Pick between all credentials on all connected YubiKeys
- No mouse interaction required


Usage
---

Invoke with `--help` to see the command line options.

    $ yubikey-oath-dmenu --help

Recommended usage is to map your preferred command line to a shortcut in your
window manager or desktop environment. For example, you could bind it to
<kbd>Super</kbd>+<kbd>o</kbd> and <kbd>Super</kbd>+<kbd>Shift</kbd>+<kbd>o</kbd>
in [i3wm][] like this:

    # Grab OTPs from ykman oath
    bindsym $mod+o exec yubikey-oath-dmenu --notify --clipboard clipboard
    bindsym $mod+Shift+o exec yubikey-oath-dmenu --notify --type


Dependencies
---

- [Python 3][python]
- [Click][click]
- [dmenu][]
- [xclip][]
- [YubiKey Manager Python library][ykman], version 0.5.0 or later.

Optional dependencies:

- [libnotify][]: For the `--notify` option, which uses `notify-send`
- [pinentry][]: To prompt for the YubiKey OATH password when needed
- [xdotool][]: For the `--type` option


Installation
---

- **Arch Linux**: [AUR package][aur]
- **Others**: Place `yubikey-oath-dmenu` somewhere on your `$PATH`.
  `/usr/local/bin/` probably works, for example.


[aur]: https://aur.archlinux.org/packages/yubikey-oath-dmenu
[click]: https://palletsprojects.com/p/click/
[dmenu]: https://tools.suckless.org/dmenu/
[i3wm]: https://i3wm.org/docs/userguide.html
[libnotify]: https://developer.gnome.org/libnotify/
[pinentry]: https://www.gnupg.org/related_software/pinentry/index.html
[python]: https://www.python.org/
[xclip]: https://linux.die.net/man/1/xclip
[xdotool]: http://www.semicomplete.com/projects/xdotool/
[ykman]: https://github.com/Yubico/yubikey-manager
[YubiKey]: https://www.yubico.com/products/yubikey-hardware/


Contributors
---

Big thanks to our contributors:

- [Andrei Gherzan](https://github.com/agherzan)
- [relatev](https://github.com/relatev)
