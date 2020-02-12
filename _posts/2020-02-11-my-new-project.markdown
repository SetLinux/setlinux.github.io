---
layout: post
title:  "My new project! (SetLinux)"
date:   2020-02-10 22:57:32 +0200
categories: setlinux 
---
Hey Everyone,
I want to introduce all of you to my little project `SetLinux` , it's a GNU/Linux distribution built from source as a new way to do GNU/Linux.
## The idea
The idea of doing this started from my dissatisfaction for the way the `FHS` worked in Linux and noticed that attempts to fix it like
Gobo and NixOS were approaching the problem from a different perspective. 

I want to approach the problem in a way so that the environment is friendlier to both users and developers.   
Now , There is difference between developers and power-users .
Not all developers are power-users and neither is the other way but I see the two terms getting mixed up quite often.
### Paying homage
Of course my idea draws a **LOT** of inspiration from (Gobolinux and NixOS) but with a different take that should be complimented with a package manager
## The File hierarchy
My intended file hierarchy is like this
```
apps/
	app-name/
		app-version/
			appfiles
```


There will be something similar to Gobo's legacy system tree so that you can run binaries directly when downloading them without patching them and without any setup.   
This hierarchy will allow my package manager to be able to even install .deb packages or rpm packages into appropriate directories easily.

## Package manager abilities
One other feature that the package manager will be able to do is locking applications at using specific library versions.
So if you have two version of ``libA`` you can set one as being the default so that all application use this version by default while you can lock some specific application to use the other version.


The package script format is going to be `Lua` so that it allows more options and easier to start working with.
The PM(Package MANAGER) will be written in `rust` so that's memory safety for you. 
There are other several reason I chose rust and I will discuss them in later posts. 

I will discuss also a couple of the challenges I had with writing the PM and I how
I approached them in later posts. 

Now this has been a very very short introduction to what the distro aims to do.  
I hope it will reach it's goals :)



Thanks for your time reading
See you soon

