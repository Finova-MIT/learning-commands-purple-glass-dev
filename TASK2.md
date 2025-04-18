# PWN COLLEGE

## MOD 1: HELLO HACKERS

### Section 1: Intro to Commands
`hacker@hello~intro-to-commands:~$ whoami`<br/>
This will print the usernames which is `hacker`<br/><br/>
`hello` command for getting the flag:
<br/>
pwn.college{UW-C4pHjTaeEldfOGacoNGVjHbQ.ddjNyUDL3ITN0czW}

### Section 2: Intro to Arguments
1. The first word is the command, and the subsequent words are arguments.
2. `echo` is a simple command that "echoes" all of its arguments back out onto the terminal.
`hello hackers` command for getting the flag:
<br/>
pwn.college{UW-C4pHjTaeEldfOGacoNGVjHbQ.ddjNyUDL3ITN0czW}

## MOD 2: PONDERING PATHS

### Section 1: The Root 
The task is to invoke the code written within the file name `pwn` which we are accessing through <br/>`/pwn` <br/>which is the absolute path.
<br/>
Flag :
pwn.college{4NOnHUZUzfpuv61148qvw32P-tS.dhzN5QDL3ITN0czW}

### Section 2: Program and absolute paths
1. To access the flag, I have to execute the code within the `run` file which inturn is within the `challenge` directory.<br/>
`hacker@paths~program-and-absolute-paths:~$ /challenge/run`<br/>
Flag :
pwn.college{QKSGf6m9CDqFCQjDOMjjKrCCabS.dVDN1QDL3ITN0czW}

### Section 3: Position thy self 
1. `hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately.`
2. `hacker@paths~position-thy-self:~$ cd /usr/share/doc/fontconfig`
3. `hacker@paths~position-thy-self:/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{IWJRKavrMWkldX-UFe5EX6cZJAk.dZDN1QDL3ITN0czW}`


### Section 4: Position Elsewhere 
```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/share/doc
hacker@paths~position-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{UMTnGI1Oh1CIEPJ8_bxq4Z-Dslb.ddDN1QDL3ITN0czW}
```
### Section 5 : Position yet elsewhere
```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /etc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /etc
hacker@paths~position-yet-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4Yi2h04rYXt1_LeQNTW6y-a3i5W.dhDN1QDL3ITN0czW}
```
### Section 6: Implicit relative paths, from /
```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{QK4612kV4bIg9iHnG_BZxBHM3iN.dlDN1QDL3ITN0czW}
```
### Section 7 : Explicit relative paths, from /
```
hacker@paths~explicit-relative-paths-from-:/$ cd /.
hacker@paths~explicit-relative-paths-from-:/$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{clm70Z3q6KxewKzwA8oL21zf-d8.dBTN1QDL3ITN0czW}
```
### Section 8: Implicit relative path
```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ run
ssh-entrypoint: run: command not found
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{EccT5RFZlYIQJmCXm9vefvqxTYJ.dFTN1QDL3ITN0czW}
```
### Section 9: Home Sweet Home
```
Note that the expansion of ~ is an absolute path, and only the leading ~ is expanded. This means, for example, that ~/~ will be expanded to /home/hacker/~ rather than /home/hacker/home/hacker.
<br/>
NOTE: cd will use your home directory as the default destination:

hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ cd
hacker@dojo:~$

hacker@paths~home-sweet-home:~$ /challenge/run ./f
The argument you provided is not an absolute path!
hacker@paths~home-sweet-home:~$ /challenge/run /f
The argument you provided is not under your home directory!
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{IWnLOT7Db7GXn-6-G5SWTqCP-6A.dNzM4QDL3ITN0czW} ```
```

## MOD 3 : COMPREHENDING COMMANDS

### Section 1: Cat, not the pet but the command
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{gdEsSmh2QwtPr1gvN_ehfFeCJqX.dFzN1QDL3ITN0czW}
```

### Section 2: catting absolute paths
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{A1RIZ_fSoPAN8fyxQcyabUDUQQ9.dlTM5QDL3ITN0czW}
```

### Section 3: more catting practice
```
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/local/share/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/local/share/flag
pwn.college{EgRtMcClCDZ3Dn7sPKEFJv2W8A-.dBjM5QDL3ITN0czW}
```

### Section 4: Grepping for a needle in a haystack
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{Y_iG683DIViRQc-5IHY06LxG4kU.ddTM4QDL3ITN0czW}
```

### Section 5: Listing files 
```
hacker@commands~listing-files:/$ ls /challenge
20135-renamed-run-20752  DESCRIPTION.md
hacker@commands~listing-files:/$ /challenge/20135-renamed-run-20752
Yahaha, you found me! Here is your flag:
pwn.college{ARFCQiKDZvGOhMyQm7nJnX5mhdO.dhjM4QDL3ITN0czW}
```

### Section 6: Touching files
```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{8iCWA69MSMIrfibVAtMBHX3KBm6.dBzM4QDL3ITN0czW}
```

### Section 7: Removing files
```
hacker@commands~removing-files:~$ ls
delete_me  f
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{IL-ui9zHMCGcaAPret9_UqHn_4z.dZTOwUDL3ITN0czW}
```

### Section 8: Hidden files
```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.           .flag-21199982310851  challenge  home   lib64   mnt  proc  sbin  tmp
..          bin                   dev        lib    libx32  nix  root  srv   usr
.dockerenv  boot                  etc        lib32  media   opt  run   sys   var
hacker@commands~hidden-files:/$ cat .flag-21199982310851
pwn.college{8mMhxN6JJozTSYa8lZoeAHY5nW8.dBTN4QDL3ITN0czW}
```
### Section 9: An epic filesystem quest
```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
BLUEPRINT  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin        challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat BLUEPRINT
Tubular find!
The next clue is in: /usr/share/racket/pkgs/racket-doc/scribblings/scheme/compiled

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/racket/pkgs/racket-doc/scribblings/scheme/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/racket-doc/scribblings/scheme/compiled$ ls
WHISPER  compat_scrbl.dep  compat_scrbl.zo  info_rkt.dep  info_rkt.zo  scheme_scrbl.dep  scheme_scrbl.zo
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/racket-doc/scribblings/scheme/compiled$ cat WHISPER
Lucky listing!
The next clue is in: /usr/share/X11/locale/el_GR.UTF-8
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/racket-doc/scribblings/scheme/compiled$ cd /usr/share/X11/locale/el_GR.UTF-8
hacker@commands~an-epic-filesystem-quest:/usr/share/X11/locale/el_GR.UTF-8$ ls
Compose  POINTER  XI18N_OBJS  XLC_LOCALE
hacker@commands~an-epic-filesystem-quest:/usr/share/X11/locale/el_GR.UTF-8$ cat POINTER
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/include/linux/phy

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/X11/locale/el_GR.UTF-8$ ls /opt/linux/linux-5.4/include/linux/phy
TEASER-TRAPPED  omap_control_phy.h  omap_usb.h  phy-mipi-dphy.h  phy-sun4i-usb.h  phy.h  tegra  ulpi_phy.h
hacker@commands~an-epic-filesystem-quest:/usr/share/X11/locale/el_GR.UTF-8$ cat TEASER-TRAPPED
cat: TEASER-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/share/X11/locale/el_GR.UTF-8$ cat /opt/linux/linux-5.4/include/linux/phy/TEASER-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/share/seabios/optionrom
hacker@commands~an-epic-filesystem-quest:/usr/share/X11/locale/el_GR.UTF-8$ cd /usr/share/seabios/optionrom
hacker@commands~an-epic-filesystem-quest:/usr/share/seabios/optionrom$ ls
SNIPPET  extboot.bin  kvmvapic.bin  linuxboot.bin  multiboot.bin  vapic.bin
hacker@commands~an-epic-filesystem-quest:/usr/share/seabios/optionrom$ cat SNIPPET
Great sleuthing!
The next clue is in: /usr/lib/x86_64-linux-gnu/ruby/2.7.0/enc/trans

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/seabios/optionrom$ cd /usr/lib/x86_64-linux-gnu/ruby/2.7.0/enc/trans
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/ruby/2.7.0/enc/trans$ ls -a
.         big5.so     ebcdic.so              emoji_sjis_docomo.so    escape.so   iso2022.so       japanese_sjis.so  transdb.so
..        cesu_8.so   emoji.so               emoji_sjis_kddi.so      gb18030.so  japanese.so      korean.so         utf8_mac.so
.DOSSIER  chinese.so  emoji_iso2022_kddi.so  emoji_sjis_softbank.so  gbk.so      japanese_euc.so  single_byte.so    utf_16_32.so
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/ruby/2.7.0/enc/trans$ cat .DOSSIER
Lucky listing!
The next clue is in: /usr/lib/debug/.build-id/1d
hacker@commands~an-epic-filesystem-quest:/usr/lib/x86_64-linux-gnu/ruby/2.7.0/enc/trans$ cd /usr/lib/debug/.build-id/1d
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/1d$ ls
43538e9bec024560d22d0c5f65a7fa043c77f6.debug  4c2fb9e0ffcfcae03642c0d6964b3fe5045d0c.debug  EVIDENCE
43cc4e650e97607e7d8f00c0945b716a0fcc8e.debug  96833980a019bc1e045e78e5cdacc77e46ef80.debug  d30df7b02168ad5433d5586568317f7dc7b8ab.debug
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/1d$ cat EVIDENCE
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/sympy/integrals/rubi/rubi_tests/tests/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/1d$ cd  /usr/lib/python3/dist-packages/sympy/integrals/rubi/rubi_tests/tests/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/integrals/rubi/rubi_tests/tests/__pycache__$ ls
BRIEF                            test_hyperbolic_sine.cpython-38.pyc          test_sine.cpython-38.pyc
__init__.cpython-38.pyc          test_inverse_hyperbolic_sine.cpython-38.pyc  test_special_functions.cpython-38.pyc
test_1_2.cpython-38.pyc          test_inverse_sine.cpython-38.pyc             test_tangent.cpython-38.pyc
test_1_3.cpython-38.pyc          test_logarithms.cpython-38.pyc               test_trinomials.cpython-38.pyc
test_1_4.cpython-38.pyc          test_miscellaneous_algebra.cpython-38.pyc
test_exponential.cpython-38.pyc  test_secant.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/integrals/rubi/rubi_tests/tests/__pycache__$ cat BRIEF
Congratulations, you found the clue!
The next clue is in: /usr/lib/debug/.build-id/dd

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/sympy/integrals/rubi/rubi_tests/tests/__pycache__$ cd /usr/lib/debug/.build-id/dd
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/dd$ ls -a
.  ..  .CUE  429eff2603e552a4d1af5e99fc6292ab86c3f8.debug
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/dd$ cat .CUE
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{M18YPLfm6I9ZC2rHZqjSwxsdU4N.dljM4QDL3ITN0czW}
hacker@commands~an-epic-filesystem-quest:/usr/lib/debug/.build-id/dd$
```
### Section 10: Making directories 
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{sOgbr7OYC9l_PKOHIeEotMpCCqN.dFzM4QDL3ITN0czW}
```

### Section 11: Finding files
```
hacker@commands~finding-files:~$ cd /
hacker@commands~finding-files:/$ find -name flag -exec cat {} +
find: ‘./tmp/tmp.MiOQGWw5Zc’: Permission denied
find: ‘./etc/ssl/private’: Permission denied
find: ‘./var/cache/apt/archives/partial’: Permission denied
find: ‘./var/cache/ldconfig’: Permission denied
find: ‘./var/cache/private’: Permission denied
find: ‘./var/lib/apt/lists/partial’: Permission denied
find: ‘./var/lib/mysql-files’: Permission denied
find: ‘./var/lib/private’: Permission denied
find: ‘./var/lib/mysql’: Permission denied
find: ‘./var/lib/mysql-keyring’: Permission denied
find: ‘./var/lib/php/sessions’: Permission denied
find: ‘./var/log/private’: Permission denied
find: ‘./var/log/apache2’: Permission denied
find: ‘./var/log/mysql’: Permission denied
find: ‘./run/mysqld’: Permission denied
find: ‘./run/sudo’: Permission denied
find: ‘./root’: Permission denied
find: ‘./proc/tty/driver’: Permission denied
find: ‘./proc/1/task/1/fd’: Permission denied
find: ‘./proc/1/task/1/fdinfo’: Permission denied
find: ‘./proc/1/task/1/ns’: Permission denied
find: ‘./proc/1/fd’: Permission denied
find: ‘./proc/1/map_files’: Permission denied
find: ‘./proc/1/fdinfo’: Permission denied
find: ‘./proc/1/ns’: Permission denied
find: ‘./proc/7/task/7/fd’: Permission denied
find: ‘./proc/7/task/7/fdinfo’: Permission denied
find: ‘./proc/7/task/7/ns’: Permission denied
find: ‘./proc/7/fd’: Permission denied
find: ‘./proc/7/map_files’: Permission denied
find: ‘./proc/7/fdinfo’: Permission denied
find: ‘./proc/7/ns’: Permission denied
cat: ./usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
cat: ./usr/local/share/radare2/5.9.5/flag: Is a directory
pwn.college{Mmk6Xo0J5aLjhE0BZaIYdxis67n.dJzM4QDL3ITN0czW}cat: ./opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag: Is a directory
cat: ./opt/radare2/libr/flag: Is a directory
cat: ./nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag: Is a directory
cat: ./nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag: Is a directory

```
### Section 12: Linking Files
```
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
ln: failed to create symbolic link '/home/hacker/not-the-flag': File exists
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{scyZ4RAbsarL6iz8mfeWEV4U4X5.dlTM1UDL3ITN0czW}
```

## MOD 4: DIGESTING DOCUMENTATION

### Section 1: Learning from documentation
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{Mw-eA0JU66R0HC2LpARISIfra9p.dRjM5QDL3ITN0czW}
```

### Section 2: Learning complex usage
```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{k2eNcZGhEcAPcjrDYu5OWKkaXMv.dVjM5QDL3ITN0czW}
```

### Section 3: Reading Manuals 
```
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                            Challenge Commands                           CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --kwhsre NUM
              print the flag if NUM is 270

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)
hacker@man~reading-manuals:~$ /challenge/challenge --kwhsre 270
Correct usage! Your flag: pwn.college{k2FwhsBSK7NMr_eBDX0a4CAyO4e.dRTM4QDL3ITN0czW}
```

### Section 4: Searching Manuals 
```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --lxdtcs // You have to search the manual to get the correct argument
Initializing...
Correct usage! Your flag: pwn.college{85AEbo1iqqktluaGpv2B4HIkR0T.dVTM4QDL3ITN0czW}
```

### Section 5: Searching for manuals
```
hacker@man~searching-for-manuals:~$ man man
MAN(1)                                                       Manual pager utils                                                      MAN(1)

NAME
       man - an interface to the system reference manuals

SYNOPSIS
       man [man options] [[section] page ...] ...
       man -k [apropos options] regexp ...
       man -K [man options] [section] term ...
       man -f [whatis options] page ...
       man -l [man options] file ...
       man -w|-W [man options] page ...

DESCRIPTION
       man is the system's manual pager.  Each page argument given to man is normally the name of a program, utility or function.  The man‐
       ual page associated with each of these arguments is then found and displayed.  A section, if provided, will direct man to look  only
       in  that section of the manual.  The default action is to search in all of the available sections following a pre-defined order (see
       DEFAULTS), and to show only the first page found, even if page exists in several sections.

       The table below shows the section numbers of the manual followed by the types of pages they contain.

       1   Executable programs or shell commands
       2   System calls (functions provided by the kernel)
       3   Library calls (functions within program libraries)
       4   Special files (usually found in /dev)
       5   File formats and conventions, e.g. /etc/passwd
       6   Games
       7   Miscellaneous (including macro packages and conventions), e.g. man(7), groff(7)
       8   System administration commands (usually only for root)
       9   Kernel routines [Non standard]

       A manual page consists of several sections.

       Conventional section names include NAME, SYNOPSIS, CONFIGURATION, DESCRIPTION, OPTIONS, EXIT STATUS, RETURN VALUE, ERRORS,  ENVIRON‐
       MENT, FILES, VERSIONS, CONFORMING TO, NOTES, BUGS, EXAMPLE, AUTHORS, and SEE ALSO.

       The following conventions apply to the SYNOPSIS section and can be used as a guide in other sections.

       bold text          type exactly as shown.
       italic text        replace with appropriate argument.
       [-abc]             any or all arguments within [ ] are optional.
       -a|-b              options delimited by | cannot be used together.
       argument ...       argument is repeatable.
hacker@man~searching-for-manuals:~$
hacker@man~searching-for-manuals:~$ man -k challenge
lbotngfdcz (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man lbotngfdcz

CHALLENGE(1)                                                 Challenge Commands                                                CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --lbotng NUM
              print the flag if NUM is 533

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                                       May 2024                                                     CHALLENGE(1)
hacker@man~searching-for-manuals:~$ /challenge/challenge --lbotng 533
Correct usage! Your flag: pwn.college{YlboSPE53EM316tSA2BGnYYK3gf.dZTM4QDL3ITN0czW}
```

### Section 6: Helpful programs
```
acker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 749
hacker@man~helpful-programs:~$ /challenge/challenge --give-the-flag 749
Correct usage! Your flag: pwn.college{AxZMgCQzrgu7ADvLe4USucS9SDN.ddjM4QDL3ITN0czW}

```
### Section 7: Help for Builtins
```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "o6tQqL0s".
hacker@man~help-for-builtins:~$ challenge --secret o6tQqL0s
Correct! Here is your flag!
pwn.college{o6tQqL0s5Nnh86SRdryFjvtodqZ.dRTM5QDL3ITN0czW}

```

## MOD 5: FILE GLOBBING

### Section 1: Matching with *
```
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kJl0G9Oc8k8XbVmuUhdznOCiWet.dFjM4QDL3ITN0czW}
```
### Section 2: Matching with ?
```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{QwyAmraIUFOGH0pwp8J4UjV_x1o.dJjM4QDL3ITN0czW}
```
### Section 3: Matching with []
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{QA-Rw21s_BEDAb3AX2tc77RQfpc.dNjM4QDL3ITN0czW}
```
### Section 4: Matching paths with []
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{cfksmTTO8957V5OKuHZiky5tg3R.dRjM4QDL3ITN0czW}
```
### Section 5: Mixing globs
```
hacker@globbing~mixing-globs:~$ cd /challenge/files/
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [ecp]*
You got it! Here is your flag!
pwn.college{styAssB7EzcOHlvGo-0j_ZAJ7DY.dVjM4QDL3ITN0czW}
```
### Section 6: Exclusionary globbing 
```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{0cbEsnrQt2VzEg-ibXxUA4r8L5E.dZjM4QDL3ITN0czW}
```

## MOD 6 : PRACTICING PIPING

### Section 1: Redirecting output
```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{U58xkNqKHVVpNBqAT9V4CD3rwSh.dRjN1QDL3ITN0czW}
```
### Section 2: Redirecting more output
```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.

hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{QsvBeNNMmB_Lu5yQyHWgl0iqKXQ.dVjN1QDL3ITN0czW}
```
### Section 3: Appending Output
```
hacker@piping~appending-output:~$ /challenge/run > /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat  /home/hacker/the-flag
m0xMYplRLUhqeoM34roB4uc.ddDM5QDL3ITN0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat  /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{8D_sm0xMYplRLUhqeoM34roB4uc.ddDM5QDL3ITN0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
```
### Section 4: Redirecting errors
```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{sysUE4ZIE7OZltJntq99Pe4y9Fg.ddjN1QDL3ITN0czW}

hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
```
### Section 5: Redirecting input
```
hacker@piping~redirecting-input:~$ touch PWN
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{0cd9RSdFz6OJ5Eg8iKASKScUKsk.dBzN1QDL3ITN0czW}
```

### Section 6: Grepping stored results
```
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
hacker@piping~grepping-stored-results:~$ cat /tmp/data.txt
hacker@piping~grepping-stored-results:~$ grep 'pwn.college' /tmp/data.txt
pwn.college{IbyYXyQLpFZtbBZmIlyGVzwaX3_.dhTM4QDL3ITN0czW}
```
### Section 7: Grepping live output
```
hacker@piping~grepping-live-output:~$ /challenge/run | grep 'pwn.college'
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{g4yP__kOtlHSr6sBlDI395AT6id.dlTM4QDL3ITN0czW}
```

### Section 8: Grepping errors
```
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{ETlmtq6oipkMWxNp3ziPPq6JAgU.dVDM5QDL3ITN0czW}
```

### Section 9: Duplicating piped data with tee
 ```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee out | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat out
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "YMxEoyvl"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret [YMxEoyvl]
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee'
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret YMxEoyvl | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{YMxEoyvl3FY7T1Yht4SNU64YO3S.dFjM5QDL3ITN0czW}
```
### Section 10: Writing to multiple programs
```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{QK5TeEhNgQhtKnCCGfdI4DSjut3.dBDO0UDL3ITN0czW}
```

### Section 11: Split-Piping stderr and stdout
```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{kZTuH8ZR6jq5Q-B3fXK93lyfMP0.dFDNwYDL3ITN0czW}
```

