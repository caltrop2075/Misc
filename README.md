# Misc
catch all for stuff

miscellaneous stuff here
--------------------------------------------------------------------------------
file.sh [-c] "filename"

complete file info, -c turns on color

$ file.sh "$HOME/.local/bin"
$HOME/.local/bin
drwxrwxr-x 3 caltrop caltrop 16384 2023-11-01 22:33
folder, inode/directory
directory

$ file.sh "$HOME/bin/caja/opn-lnk-dir.sh"
$HOME/bin/caja/opn-lnk-dir.sh
-rwxrwxr-x 1 caltrop caltrop 1679 2023-10-31 16:46
shell script, application/x-shellscript, text/plain
Bourne-Again shell script, ASCII text executable

$ file.sh "$HOME/bin/local bin"
$HOME/bin/local bin
lrwxrwxrwx 1 caltrop caltrop 24 2021-08-17 08:13
symbolic link, inode/symlink
symbolic link to $HOME/.local/bin

$ file.sh "$HOME/Documents/Shop.ods"
$HOME/Documents/Shop.ods
-rw-rw-r-- 1 caltrop caltrop 26987 2023-10-27 21:04
OpenDocument Spreadsheet, application/vnd.oasis.opendocument.spreadsheet, application/octet-stream
OpenDocument Spreadsheet

$ file.sh "$HOME/WinXP/MP4.xls"
$HOME/WinXP/MP4.xls
-rw-rw-r-- 1 caltrop caltrop 50176 2021-05-15 09:28
Microsoft Excel Worksheet, application/vnd.ms-excel, application/x-ole-storage, application/octet-stream
Composite Document File V2 Document, Little Endian, Os: Windows, Version 5.1, Code page: 1252, Author: Caltrop, Last Saved By: Caltrop, Name of Creating Application: Microsoft Excel, Create Time/Date: Sat May 15 13:34:41 2021, Last Saved Time/Date: Sat May 15 14:28:24 2021, Security: 0
--------------------------------------------------------------------------------
global.dat

used in many scripts
offers escape sequences for color & boxes
icon definitions for use with notifications
display dividers

things like icons will need modification for your system
--------------------------------------------------------------------------------
icons.sh "pattern"

copies selected icons to $HOME/temp/icons
then you can easily look through the icons

icons.sh "*tux*"
copies all tux to the temp directory
   /usr/share/icons/Mint-X/apps/96/supertux.svg
gets copied to
   $HOME/temp/icons/supertux (Mint-X_apps_96).svg

help:
copies icons to $HOME/temp/icons
allows you to find your icon easily

icons.sh [-d,-h] [pattern]
pattern "*pattern*"
-d      delete icons in temp
        bogus pattern will do the same
-h      help
        exec with no args
--------------------------------------------------------------------------------
lnk-chk.sh

checks home directory for broken links
lists possible solutions
if you're linked into the root directory no solutions will be offered
--------------------------------------------------------------------------------
