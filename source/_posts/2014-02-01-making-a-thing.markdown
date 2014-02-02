---
layout: post
title: "Making A Thing"
date: 2014-02-01 12:32:45 -0500
comments: true
categories: 
---

I recently acquired a 3D printer. I am building a project where I want some custom enclosures and a custom display and I figured what the hell, may as well get a 3D printer and print them. Turns out, 3D printing is pretty awesome. This post isn't about that project, though, that'll come later. This post is about a thing I made that I needed. I've never really designed and made a real thing before so I thought I might document the process and share it. If you have experience doing this, this will be boring, elementary, and probably wrong.

## The Thing
I collect and enjoy listening to records. I'm not an avid hipster or anything, all of my gear is 25+ years old, but it's fun. A while ago I bought a used VPI record cleaner on ebay. It is a fantastic record cleaner. It's expensive, but sometimes you can find a good deal on ebay and get it for considerably less money.

The cleaner I bought, however, did not come with the adapter that allows it to hold 7" 45 RPM records, so to date I have been unable to clean my 45s with it. VPI [makes an adapter](http://www.musicdirect.com/p-3562-vpi-165-45rpm-spindle-adapter.aspx) but it's $30 and I've never felt like spending that kind of money for a simple piece of plastic. I once tried to make one from stuff at home depot, but I messed it up and never tried again. Tonight I figured I'd print one up.

## Version 1
I broke out the calipers and made some simple measurements and threw a design together in OpenSCAD. 

{% img center /images/making-a-thing/version1.gif %}

I sent it off to the printer and immediately realized I'd made a mistake.

{% img center /images/making-a-thing/version1.jpg %}

Rookie mistake. You can't print across that much space without supports. Supports are extra structure that break away after you're done. They help the printer make overhangs and span open space like that. So I cancelled the print, went back into the slicer, and had it add supports. This time the print finished, although it was a little rough on the underside, even though it used supports. I think Makerware is a little kooky with how it designed the supports.

{% img center /images/making-a-thing/version1-printed.jpg %}

{% img center /images/making-a-thing/version1-printed-bottom.jpg %}

I was pretty excited about this because it printed and except for some minor junk on the underside it looked pretty good. Then I tried to use it.

{% img center /images/making-a-thing/version1-in-use.jpg %}

The problem here is that it's too high. The post is threaded and there's a little knurled screw piece that screws onto it to clamp everything down. The threaded post was not coming through the piece. I failed to measure and pay attention to the height of this screw. The hole was also not quite wide enough. The piece fit over the threaded portion of the screw, but not the unthreaded base, so the piece didn't quite sit all the way down.

## Version 2
Back into OpenSCAD. I lopped off the top to bring the height down. I also flipped it so that the wider radius of the cylinder was at the top. This would make it easier to grab and pull off the cleaner. I also had this brilliant idea to add a little disk at the bottom the size of the hole in a 45 to help center it. Amazing!

{% img center /images/making-a-thing/version2.gif %}

Off to the printer it went. I was concerned it needed supports because of the large opening, so I selected the option in Makerware. It, however, did not feel the need to print any. The print turned out pretty fine, though a little rough on the underside because of the long stretches.

{% img center /images/making-a-thing/version2-printed.jpg %}

{% img center /images/making-a-thing/version2-printed-back.jpg %}

This time I had the height right, there was plenty of screw for the nut to grab onto. However, I neglected to make the center hole big enough, so it still didn't quite sit all the way down.

{% img center /images/making-a-thing/version2-record.jpg %}

I also realized that the clever retainer disk I had made wasn't actually doing anything. In order to lock the record into place it would have to be below the surface of the main body. To get that to happen, I'd have to print the piece upside down, and if that were the case I don't think that disk would have printed very well at all.

{% img center /images/making-a-thing/version2-disk.jpg %}

I thought about making the disk solid all the way up but decided to just simplify, simplify, simplify.

## Version 3
I went back into OpenSCAD and decided to just make the thing a solid piece, keeping the indent in the top for the screw to rest in.

{% img center /images/making-a-thing/version3.gif %}

That printed very well with no mess ups, because it's a very simple piece.

{% img center /images/making-a-thing/version3-printed.jpg %}

{% img center /images/making-a-thing/version3-printed-back.jpg %}

I also remembered to make the screw hole bigger, so now everything fit. The screw clamped it down nice and tight. I did make a mistake though, do you see it?

{% img center /images/making-a-thing/version3-in-use.jpg %}

After lopping the top off and switching the radii I neglected to enlarge them so the bottom of the cylinder fully covered the record label. I fixed it up in the scad and STL files but decided to not print a new one. This is good enough for now and I've got other things to do.

## Lessons Learned
I learned a good deal about designing things in this process. I learned technical things about printing like using supports, the effects of infill percentage, and how  you orient pieces on the platform so they print well.

Most importantly, I think, I learned to keep the design of the thing simple. I am not a mechanical engineer or a product designer. I only barely know what I'm doing. I tried making it look pretty and fancy, but after trial and error arrived at what was essentially a cylinder of plastic with a hole in the middle. The two adornments it has (the bevelled edge and the indentation in the top) are completely functional. I will remember this while I'm designing more things.

If you happen to need this thing, you can grab it yourself from [Thingiverse](http://www.thingiverse.com/thing:239180) or from [rubyist/3d](https://github.com/rubyist/3d) on GitHub.