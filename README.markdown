# Node Version Manager

It's repository based version of [creationix's nvm](https://github.com/creationix/nvm). It means that it doesn't download tarballs but just switches tags on node.js repository and compiles needed versions.

## Installation

First you'll need to make sure your system has a c++ compiler.  For OSX, XCode will work, for Ubuntu, the build-essential and libssl-dev packages work.

To install clone it:

    git clone --recursive git@github.com/bsodzik/nvm.git ~/.nvm

To activate nvm, you need to source it from your bash shell

    . ~/.nvm/nvm.sh

I always add this line to my ~/.bashrc or ~/.profile file to have it automatically sources upon login.   
Often I also put in a line to use a specific version of node.
    
## Usage

To compile, and install the v0.4.1 release of node, do this:

    nvm install v0.4.1

And then in any new shell just use the installed version:

    nvm use v0.4.1

Or you can just run it:

    nvm run v0.4.1

If you want to see what versions are available:

    nvm ls

To restore your PATH, you can deactivate it.

    nvm deactivate

To set a default Node version to be used in any new shell, use the alias 'default':

    nvm alias default v0.4.1

## Problems

If you try to install a node version and the installation fails, be sure to delete the node downloads from src (~/.nvm/src/) or you might get an error when trying to reinstall them again or you might get an error like the following:
    
    curl: (33) HTTP server doesn't seem to support byte ranges. Cannot resume.

Where's my 'sudo node'? Checkout this link:
    
    https://github.com/creationix/nvm/issues/43
