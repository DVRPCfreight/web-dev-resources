## Steps for installing Ruby on Rails (windows)
1. [Ensure that Ruby is not already installed](#1-ensure-that-ruby-is-not-already-installed)
2. [Install Ruby](#2-install-ruby)
3. [Install Rails](#3-install-rails)
4. [Check Rails Install](#4-check-rails-install)
5. [Install Ruby DevKit](#5-install-ruby-devkit)

### 1. Ensure that Ruby is not already installed
Open the command prompt and type `ruby -v`. If Ruby responds, and if it shows a version number at or above 2.2.2, then type `gem --version`. If you don't get an error, skip Install Ruby step. Otherwise, we'll install a fresh [Ruby](#2-install-ruby).

### 2. Install Ruby
If Ruby is not installed, then download an installation package from [rubyinstaller.org](http://rubyinstaller.org/downloads/). Follow the download link, and run the resulting installer (32-bit is fine).

During install select all three options to ensure that Ruby is accessible for development purposes.

Confirm your installation by opening a new command line window using the commands in [Step 1](#1-ensure-that-ruby-is-not-already-installed).

### 3. Install Rails
Install Rails − With Rubygems loaded, you can install all of Rails and its dependencies using the following command through the command line (run command line as administrator).
``` cli
C:\> gem install rails
```
*__Note__ that this command should be run from `C:\` to access this directory simply use the command `cd c:\` prior to the command above.*

The installer will run in the command window and rails documentation installation _will_ take a long time.

### 4. Check Rails install
Use the following command to check rails version.
``` cli
C:\> rails -v
```
**Output**
``` cli
Rails 4.2.x
```

If there are no errors you are good to go! Ruby on Rails is now installed on your Windows.

### 5. Install Ruby DevKit
Goto the [rubyinstaller.org](http://rubyinstaller.org/downloads/) website and scroll down to **Development Kit** and select the version that matches your build (probably Ruby 2.0+ on 32-bit).

The download is a self-extracting archive. When you execute the file, it will ask for a destination for the files. Enter a simple path with no spaces. A recommended location would be `C:\RubyDevKit\`.

When the extraction completes, open a command line window and navigate to the folder you extracted the files to.
``` cli
cd C:\RubyDevKit
```
Auto-detect Ruby installations and add them to a configuration file for the next step.
``` cli
ruby dk.rb init
```
The response should reference your primary install of Ruby, such as `C:/Ruby22`.

Install the DevKit, binding it to your Ruby installation.
``` cli
ruby dk.rb install
```

### Summary
You did it! Everything has been installed. You should be all set with your working Ruby installation
