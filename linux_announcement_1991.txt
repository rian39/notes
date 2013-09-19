From: Linus Benedict Torvalds (torvalds@klaava.Helsinki.FI)
Subject: Linux information sheet (non-monthly posting) 
Newsgroups: comp.os.minix, comp.binaries.ibm.pc.d, comp.os.coherent, comp.os.mach, comp.os.misc, comp.unix.sysv386, comp.unix.programmers, gnu.misc.discuss
Date: 1992-01-09 05:04:05 PST 


LINUX INFORMATION SHEET
(last updated 13 Dec 1991)

1. WHAT IS LINUX 0.11
    LINUX 0.11 is a freely distributable UNIX clone.  It implements a
subset of System V and POSIX functionality.  LINUX has been written
from scratch, and therefore does not contain any AT&T or MINIX
code--not in the kernel, the compiler, the utilities, or the libraries.
For this reason it can be made available with the complete source code
via anonymous FTP.  LINUX runs only on 386/486 AT-bus machines; porting
to non-Intel architectures is likely to be difficult, as the kernel
makes extensive use of 386 memory management and task primitives.


From: Linus Benedict Torvalds (torvalds@klaava.Helsinki.FI)
Subject: Free minix-like kernel sources for 386-AT 
Newsgroups: comp.os.minix
Date: 1991-10-05 08:53:28 PST 
Do you pine for the nice days of minix-1.1, when men were men and wrote
their own device drivers? Are you without a nice project and just dying
to cut your teeth on a OS you can try to modify for your needs? Are you
finding it frustrating when everything works on minix? No more all-
nighters to get a nifty program working? Then this post might be just
for you :-)

As I mentioned a month(?) ago, I'm working on a free version of a
minix-lookalike for AT-386 computers.  It has finally reached the stage
where it's even usable (though may not be depending on what you want),
and I am willing to put out the sources for wider distribution.  It is
just version 0.02 (+1 (very small) patch already), but I've successfully
run bash/gcc/gnu-make/gnu-sed/compress etc under it. 

Sources for this pet project of mine can be found at nic.funet.fi
(128.214.6.100) in the directory /pub/OS/Linux.  The directory also
contains some README-file and a couple of binaries to work under linux
(bash, update and gcc, what more can you ask for :-).  Full kernel
source is provided, as no minix code has been used.  Library sources are
only partially free, so that cannot be distributed currently.  The
system is able to compile "as-is" and has been known to work.  Heh. 
Sources to the binaries (bash and gcc) can be found at the same place in
/pub/gnu. 

ALERT! WARNING! NOTE! These sources still need minix-386 to be compiled
(and gcc-1.40, possibly 1.37.1, haven't tested), and you need minix to
set it up if you want to run it, so it is not yet a standalone system
for those of you without minix. I'm working on it. You also need to be
something of a hacker to set it up (?), so for those hoping for an
alternative to minix-386, please ignore me. It is currently meant for
hackers interested in operating systems and 386's with access to minix.

The system needs an AT-compatible harddisk (IDE is fine) and EGA/VGA. If
you are still interested, please ftp the README/RELNOTES, and/or mail me
for additional info.

I can (well, almost) hear you asking yourselves "why?".  Hurd will be
out in a year (or two, or next month, who knows), and I've already got
minix.  This is a program for hackers by a hacker.  I've enjouyed doing
it, and somebody might enjoy looking at it and even modifying it for
their own needs.  It is still small enough to understand, use and
modify, and I'm looking forward to any comments you might have. 

I'm also interested in hearing from anybody who has written any of the
utilities/library functions for minix. If your efforts are freely
distributable (under copyright or even public domain), I'd like to hear
from you, so I can add them to the system. I'm using Earl Chews estdio
right now (thanks for a nice and working system Earl), and similar works
will be very wellcome. Your (C)'s will of course be left intact. Drop me
a line if you are willing to let me use your code.

                Linus

PS. to PHIL NELSON! I'm unable to get through to you, and keep getting
"forward error - strawberry unknown domain" or something.
