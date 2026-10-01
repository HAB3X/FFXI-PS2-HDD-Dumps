# Wanted: PS2 hard drive dumps with Final Fantasy XI / PlayOnline

If you have an old PS2 hard drive that had Final Fantasy XI or the PlayOnline Viewer
installed, please consider contributing a dump. The PS2 version shut down in 2016 and
each drive is a snapshot of the game at the date it was last patched. Every new version
we find is one that can be preserved and made playable again.

## What we're looking for
- Any PS2 HDD (official Sony 40 GB unit or other) with FFXI and/or PlayOnline Viewer installed
- Any region (US, JP, EU), any year, any patch level
- Later patch levels (2010 and after) are the rarest and most wanted
- Drives where the game was deleted are still useful; data can often be recovered

## Before you start
- Do not boot the console with the drive connected and go online or run the game.
  It can overwrite cached data.
- Do not format or "repair" the drive, even if a PC offers to.

## Making the dump
Connect the drive to a PC with an IDE-to-USB adapter.

**Windows:** use HDD Raw Copy Tool (hddguru.com) to save the whole drive as an image file.

**Linux:** find the drive with `lsblk -dp -o NAME,MODEL,SIZE`, then:

    sudo dd if=<device> conv=sync,noerror bs=4M status=progress | gzip -c > ffxi-ps2-hdd.img.gz

## Privacy: please read
A drive dump contains everything that was on the drive: PlayOnline IDs, saved logins,
mail, chat logs, friend lists, screenshots and photos. Only upload a drive that is yours,
and only if you are comfortable with that being public. If you would rather keep it
private, say so in the issue and we can arrange a private transfer and remove personal
data before anything is shared.

## Submitting
Upload the image to archive.org and post the link in the issue on this repository.
Please include: console region, roughly when the drive was last used, and whether FFXI
was still installed.
