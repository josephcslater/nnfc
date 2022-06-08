No-name File Type Converters:
=============================

| These work, are dated, but I thought I should share them. 

| The scripts in this folder are written to convert a bunch of files
  from one end of line format to another (see background). They are
  written in PERL, and PERL must be installed on your system in order to
  run them. Go to http://www.cpan.org/ports/index.html to get it for
  free. If you have a UNIX system, it's probably already installed. If
  you are running Linux, it's probably on your CD, if not already
  installed (see the UNIX section). The scripts are much shorter than
  this web page, so I'm going to be brief here.

Description:
------------

UNIX
~~~~

The files with no extension are the actual PERL code. You should be able
to install this on a UNIX machine (maybe even a Windows machine) so file
conversions can be performed on any platform. To run them:

#. The first line should be changed to point to the PERL executable on
   the UNIX system. On my UNIX system, the first line reads
   #!/usr/local/bin/perl . On yours, it's probably different. On Linux,
   the first line should (at least on my installations) be
   #!/usr/local/perl . (That period ended the sentence, don't include
   it.) If you can't find out where or if PERL is installed, type which
   perl. If it's installed, the path will be returned.
#. In the directory where all of the files are, type chmod 755 \*. This
   will set the necessary file permissions.
#. To use them, type (for example): unix2mac "filenames". Don't type the
   quotes. Just the filenames separated by spaces. You can also use
   wildcards (just like any other UNIX command). There are really two
   sets of scripts here. The scripts starting with '2' will work
   regardless of what the current EOL characters are. However, they are
   twice as slow (half as fast?) as the other files. The advantage of
   them is that they handle mixed and unknown line endings.
#. You may discard the Drop\* files. They are useful only on MacOS X.

Mac OSX
~~~~~~~

Mac Classic: If you are still using Mac Classic (pre X MacOS)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Windows
~~~~~~~

What will happen when I run a script?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The end of line characters will be converted.

Why are the files starting with '2' half as fast?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

They do the EOL conversion twice. The first time to an intermediary
format, the second to the final EOL format.

What if I have mixed line endings?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The scripts starting with '2' will change any EOL character/s to the
desired EOL characters, so although these are half as fast, they will
work nicely.

Is there any 'danger' in using these codes?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Only the ones in the 'Extras' folder. If you tend to be error prone,
don't use the script/files with 'mac2' or 'unix2' in their names (in the
extras folder). These scripts very explicitely turn carriage returns
into line feeds, and visa-versa. The problem with this approach is that
when accidentally applied to a DOS (windows) style file, you and up with
double line breaks.

What will happen if my machine crashes in the middle of a conversion?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

| a) You will have two files, the original with the same name it had
  before, plus another with the same name plus the extension .con.
  Delete the .con file and start again.
| b) You will have the .con file plus another file with the name of the
  original plus an extension like .unix or .dos. Rename the .con file to
  the original file name. Delete the other file. You are done. For the
  MacOS Classic and Windows versions: The old files, in the old ASCII
  format will have the same filename with their format attached (e.g.
  using mac2unix on temp.ps will make a file temp.ps in UNIX format, and
  put the old file in temp.ps.mac).

Other notes:
~~~~~~~~~~~~

On a PC, you will have to edit the files as they are shown in the MacOSX
distribution. If anyone ever repackages them for PC, I'll be happy to
post them. I don't have Perl installed on my PC anymore. MacOS 9 is
dying, so I'm not going to go back and fix those scripts either, but if
you have Perl, you can do it easily yourself observing the scripts (just
one line difference near the end).

Questions, comments, concerns, and better yet, improvements?

|  

Background:
-----------

UNIX® machines end lines with a linefeed. Macs® (OS 9.x and earlier) end
lines in a carriage return. PCs end line in a carriage return/linefeed.
This is done to drive the rest of the world crazy. Yes, it actually is a
conspiracy.


Other Stuff:
------------

Copyright (C) 2001 Joseph C. Slater

This program is free software; you can redistribute it and/or modify it
under the terms of the `GNU General Public
License <http://www.gnu.org/licenses/gpl.html>`__ as published by the
Free Software Foundation.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
Public License for more details.

You should have received a copy of the GNU General Public License along
with this program; if not, write to the Free Software Foundation, Inc.,
59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.

| Mac is a registered trademark of Apple Computer, Inc. UNIX is a
  registered trademark of Open Group. Windows is a registered trademark
  of MicroSoft, Inc.
|  
