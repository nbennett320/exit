### Exit[]().sh
##### Author: Samuel Ethan Kravitz
##### Coauthor: Noah Christian Bennett
----
### Table of Contents
0. [Preamble](#preamble)
1. [History](#history)
2. [Introduction](#introduction)
3. [Implementation](#implementation)
4. [Usage](#usage)
5. [Discussion](#discussion)
6. [Limitations](#limitations)
7. [Conclusion](#conclusion)
8. [Further Reasearch](#further_research)
9. [References](#references)
----
<a name="preamble"></a>

### 0. Preamble
One of the finest truths of the world is that there is no one true method to accomplish a given task. Perhaps no class of people know this truth better than programmers, who dedicate their lives to finding provacative and innovative ways to solve problems. By our nature, we are not pleased with finding the simple, "cookie cutter" way to reach our goal. To quench our thirst, we must devise an intricate approach to reach our destination. 

Exiting a terminal is a something every programmer has done thousands of times. Thousands of times, a programmer exits a terminal by clicking on the 'x' in the top right corner. This method of exiting is tried and true, battle tested, but makes for a path that has been beaten down to nothing. Fewer programmers exit their terminal session by running the shell command exit. We have decided neither of these methods are sufficient. We have decided to pave our own path, by writing our own shell script to exit a terminal session. This is the story of Exit.[]()sh.

----
<a name="history"></a>

### 1. History
The Bourne-again Shell (Bash) is a command line interpreter and language written by American computer scientist Brian Fox. The shell was designed to be a free-software alternative to the Bourne shell. Bash was initially made for the GNU Project in 1989, but is still used today as the default login shell for most Linux and MacOs distrobutions.

The Bash language syntax is a superset of the Bourne shell which it successfully replaced; Bash inherits brace expansion, command line completion, debugging, and a variety of other expressions &#8211; [one of which is the `exit` keyword](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#Bourne-Shell-Builtins), which calls for the termination of a script. Keyword `exit`'s output reflects the exit status of an executed command. Exit statuses range from 0 to 255. Exit.[]()sh's behavior will be further discussed in the [implementation section](#implementation) of this exposition.

The 'x' button and its sister-platform counterparts have been a staple in graphical user interfaces since their inception in the early 1980. This concept was first formally reseached in Stuart K. Card's, [_The Psychology of Human &#8211; Computer Interaction_](http://www-personal.umich.edu/~itm/688/wk7/CMN-ch2.PDF). In their study, Card and his colleagues refined the ever-popular concept of a _Windows, Icons, Menus, and Pointer_ interface, or _WIMP_ interface. Coined by Merzouga Wilberts, the now-antiquated acronym has been likened to the term _GUI_. As it's expanded name suggests, _WIMP_ describes the visual representation of containerized programs on the user's screen. These programs would be accessed using a pointer to click on icons or select from menus to achieve to instantiate and input to programs. The widely accessible nature of this arrangement revolutionized computer usage as we know it today &#8211; unveiling a world of virtually infinite possibilities for non-programmers, and thus allowed for rapid adoption by companies and households around the globe.

_WIMP_ is not without its flaws, however; the design has been critisized on many fronts &#8211; the foremost of which is the lack of consideration for people with disabilities. One example: _WIMP_-style user interfaces place visually impaired users at a disadvantage, especially when alternate text interfaces are not made available. Exit.[]()sh effectively overcomes this limitation, uniting all developers and end-users alike.

----
<a name="introduction"></a>

### 2. Introduction
Our approach to Exit.[]()sh aims to mesh elegance and functionality by creating a succinct script to overcome the aforementioned burden that is the 'x' button. This goal is certainly ambitious, and achieving it was no simple feat. One factor which influenced this script's implementation is legibility. It was Linus Torvalds &#8211; pioneer of the world-renowned Linux kernel &#8211; who [said](https://www.azquotes.com/quote/1372161): 
> UNIX has a philosophy, it has 25 years of history behind it, and most importantly, it has a clean core. It strives for something - some kind of beauty. <br /> - Linus Torvalds 
>
It is an unfortunate truth that many programmers sacrifice legibility for quick or easy application. However as programmers we must strive for legibility, for it is the most tangible and human aspect of coding as an art itself. To write legible code is to preserve this work of art, therefore empowering other developers to create works of their own through style, grace, and transparency. An obsessive focus on these principles combined with our core objectives rendered an extremely daunting task.

----
<a name="implementation"></a>

### 3. Implementation
According to the [Bash official documentation](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html), the [exit status](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#Exit-Status) of a command is the value returned by the _waitpid_ system call or equivalent functions. Under certain circumstances, the shell will use special values to indicate specific failure modes.

For the shell’s purposes, a command which exits with a zero exit status has succeeded. A non-zero exit status indicates failure. This seemingly counter-intuitive scheme is used so there is one well-defined way to indicate success and a variety of ways to indicate various failure modes. When a command terminates on a fatal signal whose number is _N_, Bash returns an exit status 128+_N_.

[Parameters](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#Shell-Parameters) can be passed to Bash scripts in the command line interface. Arguments are accessed inside a script with the _$_ symbol and the argument's respective index.

Our initial implementation, or first official version, of Exit.[]()sh took user arguments. While the exact original implementation was lost in a sea of notes, test scripts, and early concepts, the first official script likely looked something like this:

```
exit $1
```

Despite this implementation's bloated or otherwise needlessly complex nature, it permits users to pass their preferred exit status as an argument. For example, a user might want to terminate Exit.[]()sh with exit code _1_ as opposed to _0_. In practice this would look like:

```
user@user:~/$ sh exit.sh 1
```

User arguments do allow for more flexibility on the user's behalf, as there are simply more possible exit statuses. However we opted to take a more streamlined approach, which is only allowing the script to execute with exit code _0_. This logic behind this decision will be elaborated on in the [discussion section](#discussion).

----
<a name="usage"></a>

### 4. Usage
As we have discussed, Exit.[]()sh 

----
<a name="discussion"></a>

### 5. Discussion

----
<a name="limitations"></a>

### 6. Limitations

----
<a name="conclusion"></a>

### 7. Conclusion

----
<a name="further_research"></a>

### 8. Further Research

----
<a name="references"></a>

### 9. References
- [Bash Reference Manual ](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html)
- [Linus Torvalds Quote - AZQuotes](https://www.azquotes.com/quote/1372161)
- [The Psychology of Human &#8211; Computer Interaction - Card, Stuart K., Morgan, Thomas P., Newell, Allen](http://www-personal.umich.edu/~itm/688/wk7/CMN-ch2.PDF)
