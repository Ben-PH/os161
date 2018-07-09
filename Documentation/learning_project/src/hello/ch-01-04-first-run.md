# First Run!

This is the most exciting part. You have the binaries. You have the utilities. 
Now it's just a matter of running it. Let's get started!

### Tools

In the last section, we created the resources (binaries, file structure, etc)
that os161 runs on. This build runs on simulated hardware. System161, which we
installed during [Acquire resources](TODO).

```cmd
cd ~/os161/root/
sys161 kernel
```

If all goes well, you have your first run of an OS! AWESOME!!!!!

You should see something that looks a bit like this:
```text
sys161: System/161 release 2.0.8, compiled Feb 19 2017 14:31:53

OS/161 base system version 2.0.3
(with locks&CVs solution)
Copyright (c) 2000, 2001-2005, 2008-2011, 2013, 2014
   President and Fellows of Harvard College.  All rights reserved.

This is awesome! I should be changed, though...'s system version 0 (HELLO #1)

1892k physical memory available
Device probe...
lamebus0 (system main bus)
emu0 at lamebus0
ltrace0 at lamebus0
ltimer0 at lamebus0
beep0 at ltimer0
rtclock0 at ltimer0
lrandom0 at lamebus0
random0 at lrandom0
lser0 at lamebus0
con0 at lser0

cpu0: MIPS/161 (System/161 2.x) features 0x0
OS/161 kernel [? for menu]: 

```

At this point, have a play. Look at the different commands, try running `sys161` without any arguments, and explore. Note the message `This is awesome! I should be changed, though...`? Let's fix that :D

