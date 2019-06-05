# sqlite3_unicode

Minimal extenstion for Unicode support in Sqlite3 with no external dependencies (like libicu).

Originally from [Ioannis Epaminonda](http://www.mail-archive.com/sqlite-users@sqlite.org/msg30403.html).
Copies of [original mailing list post](msg30403.htm) and [blog entry](sqlite-native-unicode-like-support.html)
are included.

# building under macos

    $ gcc --shared -o unicode.dylib -fPIC sqlite3_unicode.c 
    $ sqlite3
    sqlite> .load unicode
    sqlite> select upper('Ура, заработало!') t;
    УРА, ЗАРАБОТАЛО!
    sqlite> 

# (not tested by me) windows and linux build

## Windows
To make build for Windows must have:
 * MS Visual Studio 2012 or newer
 * Cygwin

Run mk.cmd to build
 
Target Arch can switched in MakeFile 
M = /MACHINE:X86
M = /MACHINE:X64

## Linux and Unixes
Run mk.sh to make build
