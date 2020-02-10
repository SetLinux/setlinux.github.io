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
ofcourse my idea draws a *LOT* of inspiration from them but with a different take that should be compliminted with a package manager
that is aimed to complete the whole experience
my intended FHS is like that
``
	apps/
		app-name/
			app-version/
				appfiles
``


there will be something similar to what gobo has to have a legacy system tree so that you can run binaries directly when downloading them 
without patching them and without any setup 
now this hirachy will allow my package manager to be able to even install .deb files into their own places easily
the package format is gonna be in lua scripts so it's easy to get started writing packages,
back to the file hirachy :  
the good this about this is the cool stuff you can do like for example 
if you have two version of ``libA`` you can set one as being the default while lock some other application to use the other version

now this has been a very very short introduction to what the distro aims to do , i hope it will reach it's goals :)

thanks for your time reading , see you soon

