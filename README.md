mkinitcpio-message
==================

Displays a message during boot. Useful for showing a message or logo before
asking for luks passphrase.

To change the displayed message, edit the file at `/etc/initcpio/message`.
This file will be catted during boot.

To display your distro logo, redirect neofetch output to
`/etc/initcpio/message`.
```
# echo -en '\ec' > /etc/initcpio/message  # clear the screen before output
# neofetch -L >> /etc/initcpio/message    # display distro logo
```

Add `message` to your hooks in `/etc/mkinitcpio.conf`. To display the message
immediately before asking for luks passphrase, add the `message` hook directly
before the `encrypt` hook.
<pre>
HOOKS=(base udev autodetect keyboard keymap consolefont
       modconf <b><i>block</i></b> message encrypt lvm2 filesystems fsck)
</pre>

Rebuild your initramfs.
```
# mkinitcpio -P
```
