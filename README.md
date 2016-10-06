Learn How to Code
=================

## Project mission
This project teaches the very basics of programming:
+ variables
+ conditions (if then else)
+ arrays
+ loops
+ subprograms / functions

This is done by providing an easy to install programming environment. If you know how to use a web browser, then you are ready to follow the tutorial and do your own experiments.


## How to get started
### Installation
If you know how to insall programs on a Mac or PC, you should be able to get everything up and running. If not, ask someone to help you.

Follow these simple steps to install everything you need to start programming:
1. install [virtual box](https://www.virtualbox.org/wiki/Downloads).
* install [vargrant](https://www.vagrantup.com/downloads.html).
* Copy the [zipfile from Github](https://github.com/ptwobrussell/Mining-the-Social-Web-2nd-Edition/). And extract it somewhere.
* Use a terminal (dos-prompt / cmd) and navigate to the folder that contains the extracted files. You should find a file named `vagrantfile`.
* type in `vagrant up`. This command will prepare a "virtual computer" on your pc or mac. Everything will be installed within this "virtual computer" so there won't be any interferences with other programs on your mashine.
* type in `vagrant provision` this command may take even longer (leave it for the night). It will install a modern python development environment.

### Start the tutorial
After the installation. Use [http://localhost:8888](http://localhost:8888) in your web browser, to start the environment. Click on the first lesson to start the tutorial.

## Stoping and resuming
* Use `vagrant status` to check whether the vagrant machine is up and running.
* start and stop vagrant via `vagrant up` and `vagrant halt` (do not use `vagrant suspend` in most cases)
* Use `vagrant destory` if you have to restart completly from scratch or have to reuse the disk space.

## Behind the scenes
* Vagrant is used to install python 3, jupyter and some other tool from the Anaconda eco system to a virtual mashine.
* Vagrant is instructed to use chef as the provisioner.
* The virtual mashine is provided via Oracles virtual box.
* A web server is running on the virtual (guest) computer. This server serves the jupyter notebooks.
* These notebooks can be accessed via port forwading from the host computer.
* This way all the tutorials are brought to the users browser.

## Get in touch
* Use Github to open tickets for support questions.
* Follow me on Twitter `@r_rbn`
* Tweet using `#lhtc` (learn how to code). Or send me a DM.
* Forking, starring, following the github repo would be great.

## Inspired by the ZX81
35 years ago I started programming on a ZX81. Since then I never stopped. Now my son is the same age as I was then. He starts to program  on his iPod (although he owns a desktop PC). Why is this? It should be so much easier to program with an IDE using a modern programming language ...

Really? Thinking back, the ZX81 was the ideal platform to learn how to code:

+ No need to learn about files and folders, file-systems explorers, access control lists, file names and suffices. There was only one program in memory that could be executed.
+ No need to learn a lot of computer language. All Sinclair-basic commands where printed on the keyboard. You would access them via "hot keys", so no misspelling. No syntax errors.
+ No need to learn how to work with a complex editor and switching between editor, compiler and console / browser. No need to learn to work with an IDE. Rudimentary editing of the one and only program in memory and executing this program, was the only way the ZX81 could operate.
+ A modern beginners programming book for JavaScript has a couple of hundreds of pages. The ZX81 got 90 pages, 30 of which for reference.
+ Nowadays the beginner has to master html and JavaScript. He has to take care of CSS for the layout in the browser. The ZX81 could hold max 1 kB (yes, no misspelling here) of source code, so there was no way to do fancy GUI stuff (and no need to do so either).

So this project is about ultimate simplicity. How can we teach the basics of programming: variables, conditions, loops and "subprograms"?

This project is not aiming at a nostalgic ZX81-emulation. On the contrary I will use Python 3.X, jupyter with the Anaconda ecosystem to prepare a learning platform via vagrant / chef on a virtual mashine.

The goal is to prepare an easy set up of an development environment that can be used via the browser. And to provide a set of simple jupyter playbooks. Aimed at the beginner to teach them the basics.

This work is inspired by Matthew A. Russel's work on [Mining the social Web](https://miningthesocialweb.com), where I found out about iPython (now jupyter) and how to use Vagrant and chef to prepare an easy to deploy development environment.

![The ZX81](images/ZX81.jpg)

## Status
* The vagrantfile is done, so setting up the development environment is working. Some tweeks to the chef recipes have been necessary to point the jupyter working directory to the right directory that is linked from the guest machine directly to the host machine.
* The first lesson on statements and expressions is finished.
