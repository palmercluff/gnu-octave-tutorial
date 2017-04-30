# gnu-octave-tutorial
A tutorial for those wanting to learn GNU Octave.

### References
- GNU Octave Beginners Guide by Jesper Schmidt Hansen (https://www.amazon.com/Octave-Beginners-Jesper-Schmidt-Hansen/dp/1849513325)

## Introduction
GNU Octave is a high-level, multi-functional scientific tool used for numerical analysis. In the broad sense, it is a numerical computing environment and programming language similar to MATLAB. In fact, it's so similar that some call GNU Octave a MATLAB "clone" because most MATLAB scripts can be ran by GNU Octave. One key difference to note right off the bat is unlike MATLAB, GNU Octave is free, so it makes for a great alternative. MATLAB liscenses typically cost around $50 if you are a student or $150 if you are a home user, so if you don't want to spend money but still be able to do scientific computing and data analysis, read on!

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

At the prompt, you can type `exit` then press enter, or do CTRL + D to quit the interpreter. Great! We are ready to move on.

## First Execution
Let's test out Octave and do something cool! Let's try making some plots to see what Octave is capable of. Get back into Octave by typing `octave` in your console, then at the prompt, type the following below (don't type `octave:1>`, that's just part of the program):

`octave:1> surf(peaks)`

![alt text](https://github.com/palmercluff/gnu-octave-tutorial/blob/master/surf_peaks.png "Picture 1")

You should see a 3-D surface plot graphical window come up. Cool, right!? Don't worrk if you don't know much about graphing or plotting stuff, we just wanted to make sure this worked. Let's try another one! (Remember, just type: "contourf(peaks)" at the prompt)

`octave:2> contourf(peaks)`

![alt text](https://github.com/palmercluff/gnu-octave-tutorial/blob/master/contourf_peaks.png "Picture 2")

Pretty neat, huh? As you may have noticed, every time you enter a valid command or function, the number within the prompt increments by 1. This isn't really importnat, but just thought I would point it out. You can also hit the up arrow key while in the program to see past commands you ran. Pretty nifty!

## Basic Programming
In order to tell Octave what we want it to do, we need to do some programming. Later on, we will learn how to make scripts (a file used to help automate programming tasks) but for now, we are just going to keep typing things into the console.

Just like in Mathematics, if we want to store some sort of value, we need container called a "variable". In Octave, a variable has two properties, a name and a value. For example, If we wanted to store the number 10 in 'x', then our variable name is 'x' and our value is 10. In Octave, it would look something like this:

```
octave:1> x=10
x =  10
```

What this did is store 10 into 'x'. When we typed `x=10` in the prompt and hit enter, the program evaluated it and outputted what 'x' holds. Now if you return to the prompt and type 'x' then press enter like so:

```
octave:2> x
x =  10
```

It will give back what 'x' holds. Nifty!

Variables can hold lots of different things, including but not limited to scalers, vectors, and matrices (linear algebra-type stuff). We can have a variable hold an array (a group of values that are similar to each other), a row vector, or a column vector.

```
octave:1> array = [1 2 3]
array =

   1   2   3

octave:2> row_vector = [1, 2, 3]
row_vector =

   1   2   3

octave:3> column_vector = [1;2;3]
column_vector =

   1
   2
   3
```

We could even create a 2 x 3 matrix with two rows and three columns:

```
octave:1> two_by_three_matrix = [1 2 3; 4 5 6]
two_by_three_matrix =

   1   2   3
   4   5   6
```

Notice how I have underscores between my variable names? You can't have spaces in a variable name otherwise you will get errors.

We can also access a single element, or number within an array. If we wanted to access the second element:

```
octave:1> a = [2 4 6 8 10]
a =

    2    4    6    8   10

octave:2> a(2)
ans =  4
```

we do `a(2)` and it gives us the number 4 because that was the second element in the array (from left to right). If we look back at our two_by_three_matrix variable and we wanted to get the number that lies in the second row, third column, we would do something like this:

`two_by_three_matrix(2,3)` and it would give us an `ans = 6`

If we wanted to get the entire second column, we would do `two_by_three_matrix(:,2)`, and if we wanted the entire 1st row, we would do `two_by_three_matrix(1,:)`

If we want to change a value in an array or matrix, simply use the parenthesis and use an equal sign. For example, looking back at our 'a' variable/array, we can say `a(2) = 10` and it would make the second element hold 10!