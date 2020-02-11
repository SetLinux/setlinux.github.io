---
layout: post
title:  "My new project! (SetLinux)"
date:   2020-02-10 22:57:32 +0200
categories: jekyll update linux project rust dev
---
Hey Everyone,
i wanna introduce all of you to my little project `SetLinux` , it's a linux distrobution built from source as a new way to do linux.
the idea of doing it started from my un-satisfaction with the way the `FHS` worked in linux and noticed that attempts to fix it like
Gobo and NixOS are hitting the problem from a different prespective ,
i want to hit the problem in a way so that the environment is more user-friendly and developer-friendly   
now there is difference between being developer friendly and being power-users friendly , not all developers are power-users which is a confusion i saw getting made fairly often

ofcourse my idea draws a *LOT* of inspiration from (gobolinux and NixOS) but with a different take that should be compliminted with a package manager
my intended file hirachy is like that
```
	apps/
		app-name/
			app-version/
				appfiles
```


there will be something similar to what gobo's legacy system tree so that you can run binaries directly when downloading them without patching them and without any setup   
now this hirachy will allow my package manager to be able to even install .deb packages or rpm packages into their own places easily

back to the file hirachy :  
the good this about this is the cool stuff you can do like for example 
if you have two version of ``libA`` you can set one as being the default while lock some other application to use the other version


the package format is lua scripts so it's easy to get started writing packages,
the PM(Package MANAGER) will be written in `rust` so that's memory safety for ya 
there are other several reason i chose rust and i will discuss them in later posts 

i will discuss also a couple of the challenges i had with writing the PM and i how
i approached them in later posts 

now this has been a very very short introduction to what the distro aims to do , i hope it will reach it's goals :)



thanks for your time reading , see you soon

