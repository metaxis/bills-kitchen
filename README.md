
Bill's Kitchen
==============

All you need for cooking with Chef and Vagrant on Windows, shrink-wrapped in a portable package:

 * pre-configured Chef Repo with Vagrantfile to bring up a ready-to-use Chef Server 
 * devkit enhanced Ruby 1.9.3 with the following gems pre-installed:
 	* vagrant (patched to make `vagrant ssh` work on windows)
 	* chef
 	* librarian
 	* veewee
 	* sahara (patched to work on windows)
 	* foodcritic
 	* cucumber-nagios
 	* knife-solo (patched to work on windows)
 * supporting tools such as:
 	* Console2 (with ansicon)
 	* SublimeText2 (with additional packages for Chef and Cucumber)
 	* PortableGit (preconfigured with kdiff3 as diff/merge tool)
 	* putty
 * walkthrough tutorial and example cookbooks

The only requirement for using the devpack is a recent version of [VirtualBox](https://www.virtualbox.org/wiki/Downloads) (couldn't make that one portable).


Installation
============

As a prerequisite for building bill's kitchen you need 7zip installed in `C:\Program Files\7-Zip\7z.exe`. 

Build the kitchen:

```
gem install bundler
bundle install
rake build
```

This might take a while (you can go fetch a coffee). It will download the external dependencies and assemble the kitchen in the `target/build` directory, which is then packaged as `target/bills-kitchen-<version>.7z`

								
Usage
=====

Make sure you have  [VirtualBox](https://www.virtualbox.org/wiki/Downloads) installed, then:

1. unzip the `target/bills-kitchen-<version>.7z` somewhere
2. mount the kitchen to the `W:\` drive by double-clicking the `mount-w-drive.bat` file
3. click `W:\Launch Console.lnk` to open a command prompt
4. in the command prompt run `W:\set-env.bat` to set up the PATH etc 
5. walk through the [GETTING_STARTED.html](file://W:/_GETTING_STARTED.html) tutorial and start cooking!

