[https://www.theopensourceway.org/wiki/How_to_tell_if_a_FLOSS_project_is_doomed_to_FAIL]

# Size
* The source code is more than 100 MB. ~[ +5 points of FAIL ]~
* If the source code also exceeds 100 MB when it is compressed ~[ +5 points of FAIL ]~

# Source Control
* There is no publicly available source control (e.g. cvs, svn, bzr, git) ~[ +10 points of FAIL ]~
* There is publicly available source control, but:
  * There is no web viewer for it ~[ +5 points of FAIL ]~
  * There is no documentation on how to use it for new users ~[ +5 points of FAIL ]~
  * You've written your own source control for this code ~[ +30 points of FAIL ]~
  * You don't actually use the existing source control ~[ +50 points of FAIL ]~

# Building From Source
* There is no documentation on how to build from source ~[ +20 points of FAIL ]~
* Documentation exists on how to build from source, but it doesn't work ~[ +10 points of FAIL ]~
* The source is configured:
  * with a handwritten shell script ~[ +10 points of FAIL ]~
  * by editing flat text config files ~[ +20 points of FAIL]~
  * by editing code header files manually ~[ +30 points of FAIL ]~
* The source isn't configurable ~[ +50 points of FAIL ]~
* The source builds:
  * using something that isn't GNU Make **[ +10 points of FAIL ]**
  * only with third-party proprietary build tools ~[ +50 points of FAIL ]~
  * with your own build tool for this code ~[ +100 points of FAIL ]~
* The build has no tests ~[ +5 points of FAIL ]~

~Java has some different rules, as the language capabilities are different than many other environments:~
* ~The build process doesn't use a standard build tool like Ant, Maven, Gradle [ +10 points of FAIL ]~
* ~The runtime artifacts rely on native libraries [ +5 points of FAIL ]~
* ~The build has no tests [ +20 points of FAIL ]~

# Bundling
* Your source only comes with other code projects that it depends on ~[ +20 points of FAIL ]~
* If your source code cannot be built without first building the bundled code bits ~[ +10 points of FAIL ]~
* If you have modified those other bundled code bits ~[ +40 points of FAIL ]~

# ~Libraries~
* ~Your code only builds static libraries [ +20 points of FAIL ]~
* ~Your code can build shared libraries, but only unversioned ones [ +20 points of FAIL ]~
* ~Your source does not try to use system libraries if present [ +20 points of FAIL ]~

~For Java:~
* ~Your code builds native deliverables [ +5 points of FAIL ]~

# System Install
* Your code tries to install into /opt or /usr/local ~[ +10 points of FAIL ]~
* Your code has no "make install" **[ +20 points of FAIL ]**
* Your code doesn't work outside of the source directory ~[ +30 points of FAIL ]~

# Code Oddities
* Your code uses Windows line breaks ("DOS format" files) ~[ +5 points of FAIL ]~
* Your code depends on specific compiler feature functionality **[ +20 points of FAIL ]**
* Your code depends on specific compiler bugs ~[ +50 points of FAIL ]~
* Your code depends on Microsoft Visual Anything ~[ +100 points of FAIL ]~

# Communication
* Your project does not announce releases on a mailing list **[ +5 points of FAIL ]**
* Your project does not have a mailing list **[ +10 points of FAIL ]**
* Your project does not have a bug tracker ~[ +20 points of FAIL ]~
* Your project does not have a website ~[ +50 points of FAIL]~
* Your project is sourceforge vaporware ~[ +100 points of FAIL ]~

# Releases
* Your project does not do sanely versioned releases (Major, Minor) ~[ +10 points of FAIL ]~
* Your project does not do versioned releases ~[ +20 points of FAIL ]~
* Your project does not do releases ~[ +50 points of FAIL ]~
* Your project only does releases as attachments in web forum posts ~[ +100 points of FAIL ]~
* Your releases are only in .zip format ~[ +5 points of FAIL ]~
* Your releases are only in OSX .zip format ~[ +10 points of FAIL ]~
* Your releases are only in .rar format ~[ +20 points of FAIL ]~
* Your releases are only in .arj format ~[ +50 points of FAIL ]~
* Your releases are only in an encapsulation format that you invented. ~[ +100 points of FAIL ]~
* Your release does not unpack into a versioned top-level directory (e.g. glibc-2.4.2/ ) ~[ +10 points of FAIL ]~
* Your release does not unpack into a top-level directory (e.g. glibc/ ) ~[ +25 points of FAIL ]~
* Your release unpacks into an absurd number of directories (e.g. home/johndoe/glibc-svn/tarball/glibc/src/) ~[ +50 points of FAIL ]~

# History
* Your code is a fork of another project ~[ +10 points of FAIL ]~
* Your primary developers were not involved with the parent project ~[ +50 points of FAIL ]~
* Until open sourcing it, your code was proprietary for:
  * ~1-2 years [ +10 points of FAIL ]~
  * ~3-5 years [ +20 points of FAIL ]~
  * ~6-10 years [ +30 points of FAIL ]~
  * ~10+ years [ +50 points of FAIL ]~

# Licensing
* Your code does not have per-file licensing ~[ +10 points of FAIL ]~
* Your code contains inherent license incompatibilities ~[ +20 points of FAIL ]~
* Your code does not have any notice of licensing intent ~[ +30 points of FAIL ]~
* Your code doesn't include a copy of the license text ~[ +50 points of FAIL ]~
* Your code doesn't have a license ~[ +100 points of FAIL ]~

# Documentation
* Your code doesn't have a changelog ~[+10 points of FAIL]~
* Your code doesn't have any documentation ~[ +20 points of FAIL ]~
* Your website has no examples of use ~[ +20 points of FAIL ]~
* Your website doesn't have any documentation ~[ +30 points of FAIL ]~

# FAIL METER
0 points of FAIL: Perfect! All signs point to success!<BR>
5-25 points of FAIL: You're probably doing okay, but you could be better.<BR>
30-60 points of FAIL: Babies cry when your code is downloaded<BR>
**65-90 points of FAIL: Kittens die when your code is downloaded<BR>**
95-130 points of FAIL: HONK HONK. THE FAILBOAT HAS ARRIVED!<BR>
135+ points of FAIL: So much fail, your code should have its own reality TV show.<BR>

# Personal notes on FAIL METER
* 50 of the 65 FAIL points are for the use of the SCons build system.
  From a quick look at what they're using (and why), I don't think this is a problem.
  I also defer to the [Introduction to the buildsystem](https://godot.readthedocs.io/en/3.0/development/compiling/introduction_to_the_buildsystem.html) docs page intro
