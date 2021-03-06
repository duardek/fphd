
# Introduction to FPGA Programming <br/> _Using Xilinx Vivado and VHDL_

## PhD Degree in Physics, University of Torino

Git repository for the [_Introduction to FPGA Programming Using Xilinx Vivado and VHDL_](http://dottorato.ph.unito.it/courses.html) (3 CFU)<br/>
PhD course at University of Torino, Physics Department.

<br/>
Lecture slides are available at :

**<http://personalpages.to.infn.it/~pacher/didattica/dottorato/FPGA/slides>**

<br/>
Additional software components for Windows can be downloaded from :

**<http://personalpages.to.infn.it/~pacher/didattica/dottorato/FPGA/software>**
<br/>
<br/>

Links to **recorded video lectures** are listed in the [**Webex lectures**](#webex-lectures) section.<br/><br/>

>
> **IMPORTANT !**
>
> All students are requested to **complete the preparatory work** before attending practical lectures !<br/>
> Please go through detailed step-by-step instructions presented in [**labs/lab0/README.md**](labs/lab0/README.md)
>


# Contents

* [**Environment setup**](#environment-setup)
* [**Git configuration**](#git-configuration)
* [**Repository download**](#repository-download)
* [**Create your personal development branch**](#create-your-personal-development-branch)
* [**Basic git commands**](#basic-git-commands)
* [**Sample simulation and implementation flows**](#sample-simulation-and-implementation-flows)
* [**References**](#references)
* [**Webex lectures**](#webex-lectures)


# Environment setup
[**[Contents]**](#contents)

In this introductory course we will adopt a **script-based** and **command-line based** approach
to FPGA programming using Xilinx Vivado assuming a **Linux-like development environment**.

Both Linux and Windows operating systems are supported. 
Familiarity with **Linux basic shell commands** to work with files and directories (`cd`, `pwd`, `mv`, `mkdir`, `rm` etc.)
with the **GNU Makefile** (`make`) and with a **text editor** is therefore assumed. 

Sample scripts `sample/bashrc` and `sample/cshrc` for Linux, as well as `sample/login.bat` for Windows are provided to
support both `csh/tcsh` and `sh/bash/zsh` Linux shells and the Windows _Command Prompt_.

Detailed **step-by-step instructions** are provided in form of a [_"lab zero"_](labs/lab0/README.md)
to help students to setup a suitable development environment for both Linux and Windows operating systems.


# Git configuration
[**[Contents]**](#contents)

### Linux installation

In case `git` is not installed on your machine, use

```
% sudo yum install git
```

or

```
% sudo apt-get install git
```


### Windows installation

For Windows users, download and install **Git for Windows** from the project official page : 

```
https://gitforwindows.org
```


### Initial configuration

The first time you use `git`, type:

```
% git config --global user.name "Your Name"
% git config --global user.email your.email@example.com
```

You can check your configuration at any time with:

```
% git config --list
```


# Repository download
[**[Contents]**](#contents)

Download the repository using:


```
% cd Desktop
% git clone https://github.com/lpacher/fphd.git [optional target directory]
```

By default a new `fphd/` directory containing the repository will be created where you invoked the above `git` command, unless
you specify a different target directory as optional parameter.

As an example :


```
% cd Desktop
% git clone https://github.com/lpacher/fphd.git FPGA
```


You can create a `git root` alias to easily locate the Git top-level directory:

```
% cd fphd
% git config --global alias.root "rev-parse --show-toplevel"
% git root
```

For setting up the proper command-line runtime environment, refer to section [**Environment setup**](#environment-setup).

** **WARN:** All `git` commands **must be invoked** inside the top `fphd/` directory or from any other sub-directory of the repository !


# Create your personal development branch
[**[Contents]**](#contents)

By default, the first time you download the repository you are in the `master` branch.
The `master` branch should always represent the "stable version" of the project :

```
% git branch
*master
```

The asterisk indicates the **current working branch**.


As a first step after downloading the repository for the first time
**create your personal development branch** named `student` :

```
% git branch student
% git checkout student
```

You can now **list all branches** in your local machine with :

```
% git branch
master
*student
```

Please, be sure that the asterisk now points to your own development branch `student` and not to the `master` branch.


# Basic git commands
[**[Contents]**](#contents)

A small collection of most frequently used `git` **command-line syntax** for your day-to-day work and common tasks can be found [**here**](doc/git/README.md).
A more complete guide to the basic `git` commands can be found [**here**](http://doc.gitlab.com/ee/gitlab-basics/start-using-git.html).


# Sample simulation and implementation flows
[**[Contents]**](#contents)

A small VHDL design example is provided to **test your environment setup** and **tools installation**.<br/>
Step-by-step instruction explaining how to run this test flow can be found [**here**](test/README.md).


# References

VHDL programming :<br/>

* B. Mealy and F. Tappero, [_Free Range VHDL_](http://freerangefactory.org/pdf/df344hdh4h8kjfh3500ft2/free_range_vhdl.pdf) (open source)
* C.H. Roth Jr, _Digital Systems Design Using VHDL_
* V.A. Pedroni, _Circuit Design with VHDL_
* R.E. Haskell and D.M. Hanna, _Introduction to Digital Design Using Digilent FPGA Boards - Block Diagram/VHDL Examples_
* P.P. Chu, _FPGA Prototyping By VHDL Examples_

FPGA programming using Xilinx Vivado :<br/>

* Xilinx official documentation (open)
* S. Churiwala (Editor), _Designing with Xilinx FPGAs Using Vivado_

Design constraints :<br/>

* S. Gangadaran and S. Churiwala, _Constraining Designs for Synthesis and Timing Analysis: A Practical Guide to Synopsys Design Constraints (SDC)_


<br/>

A list of of common acronyms and abbreviations relevant to electronics engineering and FPGA programming<br/>
can be found [**here**](doc/LOA.md).


# Webex lectures
[**[Contents]**](#contents)

Due to the COVID-19 emergency all lectures will be held **remotely** using the **Webex UniTO** platform.<br/>
All lectures will be also **video-recorded**.

The virtual room to attend the lectures is accessible at the following link :

**<https://unito.webex.com/meet/luca.pacher>**

* Lecture 1<br/>
<https://unito.webex.com/recordingservice/sites/unito/recording/play/efa1c2b298a84011859cc0b997c29cff>

* Lecture 2<br/>
<https://unito.webex.com/recordingservice/sites/unito/recording/play/e05a1454e0a549f4a30c9241923224e2>

* Lecture 3 - **TODO**

