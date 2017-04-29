# gnu-octave-tutorial
A tutorial for those wanting to learn GNU Octave.

## Introduction
GNU Octave is a high-level, multi-functional scientific tool used for numerical analysis. In the broad sense, it is a numerical computing environment similar to MATLAB. In fact, it's so similar that some call GNU Octave a MATLAB "clone" because most MATLAB scripts can be ran by GNU Octave. One key difference to note right off the bat is unlike MATLAB, GNU Octave is free, so it makes for a great alternative. MATLAB liscenses typically cost around $50 if you are a student or $150 if you are a home user, so if you don't want to spend money but still be able to do scientific computing and data analysis, read on!

### What to Expect from this Tutorial
We will assume that you haven't done very much programming, and we will refer to GNU Octave as just "Octave".

## Installing Octave
Octave is availabe for most platforms (Windows, Mac OS X, Linux). I will be showing you instructions on how to install Octave on a Debian-based Linux machine, so if you are not working on Linux, you may have to Google how to set it up.

As root, type: `apt-get install octave` in your console.

After a few short lines of text from the console, with any luck Octave should be installed. To see if it is installed, type: `octave` in the console, and the octave interpreter (program) should be running and you should see something similar to the following below:

```
GNU Octave, version 3.8.2
Copyright (C) 2014 John W. Eaton and others.
This is free software; see the source code for copying conditions.
There is ABSOLUTELY NO WARRANTY; not even for MERCHANTABILITY or
FITNESS FOR A PARTICULAR PURPOSE.  For details, type 'warranty'.

Octave was configured for "x86_64-pc-linux-gnu".

Additional information about Octave is available at http://www.octave.org.

Please contribute if you find this software useful.
For more information, visit http://www.octave.org/get-involved.html

Read http://www.octave.org/bugs.html to learn how to submit bug reports.
For information about changes from previous versions, type 'news'.

octave:1>

```