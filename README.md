# wad2svg #

## What is it? ##

A Doom level can be represented by a two-dimensional top-down map,
such as that shown on the in-game automap display. Various standalone
utilities exist for drawing a map of a Doom level. However no direct
utility for creating an SVG map of a Doom level existed, to my
knowledge, so I wrote one.

   SVG stands for Scalable Vector Graphics, the [2]new standard from the
   W3C for vector graphics on the Internet. SVG ties in with other web
   standards, so for instance it would be possible to start with a SVG
   graphic of a Doom level, and create hyperlinked parts of the image to
   screenshots (wad2svg doesn't make use of any of this cool stuff
   itself, what you use the images for is down to you).

   wad2svg is designed to be easily extensible to allow a wide range of
   different level components to be drawn, and command line parameters
   control which are drawn and options to use. Currently it supports:
     * Drawing walls and openings - this is the default, similar to
       Doom's automap
     * Drawing the nodes - the subdivisions of the level that Doom uses
       for rendering. Useful for me because I maintain a node building
       utility, and might be useful to people who have really big levels
       with visplanes problems.

   As and when I come up with other things to draw, they may be added. Of
   course, if you know some perl programming, you can write more output
   types yourself.

   Incidentally, wad2svg is written in perl, and includes a couple of
   handy perl modules for reading Doom WADs and levels. These are rather
   incomplete but may be a good basis for other perl Doom programs.

   Note that wad2svg is not a Doom level map viewer. It only creates a
   map in SVG format, it doesn't give you a way to view SVG files. See
   the [3]W3C's list of SVG viewer applications. Also, just because it
   generates an SVG image doesn't mean you can't convert it to a raster
   image afterwards, there are tools available that can do this.

Download & Updates

   wad2svg requires [4]perl, and the [5]SVG.pm module installed - either
   dump it in the directory with wad2svg, or install it on the system in
   the usual way. On Unix or Linux systems wad2svg should be very easy to
   get working once you have SVG.pm. Windows systems do not normally come
   with perl however, so unless you know how to get perl working on your
   system (or have a Unix shell you can use somewher), you can't use
   wad2svg - don't email me asking for help, I have never used perl on
   Windows either. Use a decent operating system already.

   The latest version of wad2svg is currently available from the [6]BSP
   sourceforge page. This site also carries older versions, bug reports,
   and such. You can also register to be automatically notified of new
   releases.

   The latest information about wad2svg is available from the [7]wad2svg
   homepage (which may be where you are reading this file!). There is
   also a [8]example map for those of you with SVG enabled browsers (or
   supporting program), and for those of you that don't, a [9]screenshot
   of a map loaded into an SVG editor.

Use

     ./wad2svg [ -options ] input.wad > output.svg

   The following options are available:

   -m mapname
          Selects the level to generate the map of (default MAP01)

   -d outputtype1:outputoptions1;outputtype2:outputoptions2;...
          Sets the different outputs to include in the map. The default
          is 1slines:colour=black;2slines:colour=grey. If you want the
          nodes to be displayed, add ;nodes

Author & Feedback

   wad2svg is written by [10]Colin Phipps - see the file AUTHORS included
   in the distribution for more details.

   Feedback is welcome. If people write their own output types for
   wad2svg which could be useful for others, then contributed code is
   particularly appreciated.

References

   1. http://sourceforge.net/
   2. http://www.w3.org/Graphics/SVG/
   3. http://www.w3.org/Graphics/SVG/SVG-Implementations.htm8#viewer
   4. http://www.perl.com/
   5. http://www.roasp.com/
   6. http://sourceforge.net/projects/doombsp
   7. http://doombsp.sourceforge.net/wad2svg/
   8. http://doombsp.sourceforge.net/wad2svg/example.svg.gz
   9. http://doombsp.sourceforge.net/wad2svg/example.png
  10. mailto:cph@cph.demon.co.uk
