---
layout: post
title:  "My new project! (SetLinux)"
date:   2020-02-10 22:57:32 +0200
categories: setlinux 
---
Hey Everyone,
I wanna introduce all of you to my little project `SetLinux` , it's a GNU/Linux distribution built from source as a new way to do GNU/Linux.
## The idea
the idea of doing it started from my in-satisfaction with the way the `FHS` worked in Linux and noticed that attempts to fix it like
Gobo and NixOS are hitting the problem from a different perspective ,

I want to hit the problem in a way so that the environment is more user-friendly and developer-friendly   
now there is difference between being developer friendly and being power-users friendly , not all developers are power-users which is a confusion I saw getting made fairly often
### paying homage
Ofcourse my idea draws a *LOT* of inspiration from (gobolinux and NixOS) but with a different take that should be complimented with a package manager
## The File hierarchy
my intended file hierarchy is like that
```
	apps/
		app-name/
			app-version/
				appfiles
```


There will be something similar to gobo's legacy system tree so that you can run binaries directly when downloading them without patching them and without any setup   
now this hirachey will allow my package manager to be able to even install .deb packages or rpm packages into their own places easily

## package manager abilities
One other feature that the package manager will be able to do is for example  
if you have two version of ``libA`` you can set one as being the default while lock some other application to use the other version


The package script format is gonna be lua so that it allows more options and easier to start working with,
the PM(Package MANAGER) will be written in `rust` so that's memory safety for ya 
there are other several reason I chose rust and I will discuss them in later posts 

I will discuss also a couple of the challenges I had with writing the PM and I how
I approached them in later posts 

now this has been a very very short introduction to what the distro aims to do , I hope it will reach it's goals :)



thanks for your time reading , see you soon

