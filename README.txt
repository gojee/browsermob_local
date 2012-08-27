Neustar Web Performance Script Validator
Copyright (c) 2011 Neustar, Inc.

1.  Introduction
2.  Native Mouse and Keyboard Integration
3.  Usage

1.  Introduction

The Neustar Web Performance Script Validator may be used to perform validation of JavaScript test scripts.

There are two directories:

bin - contains the execution scripts used to run the validator
lib - contains the Java libraries and third party components

2.  Native Mouse and Keyboard Integration

In order to use native mouse and keyboard integration you will need to complete the installation by downloading a copy of the open source browsermob-vnc library and installing it in the lib directory.
(see the BrowserMob blog for more details: http://blog.browsermob.com/2009/12/flash-and-flex-automation-options-using-selenium/)

You can download a copy of the Open Source BrowserMob VNC library here:

http://search.maven.org/remotecontent?filepath=org/browsermob/browsermob-vnc/1.0-beta-1/browsermob-vnc-1.0-beta-1.jar

Once downloaded, copy the file to the lib directory.

Before you can use the VNC library, you need to have a VNC server running (e.g. "Vine Server" for OS X, or "Ultra VNC" for Windows).


3.  Usage

The validator accepts parameters as documented using the "-?" option

EXAMPLE:

cd bin
validator -?
Neustar Web Performance Script Validator 1.1
Copyright (c) Neustar Inc - All Rights Reserved.
usage: validator script.js [options]
 -?            			Help
 -firebug		      	Launch with Firebug
 -browser <arg>			Specify browser to use (e.g. FF)
 -keepbrowseronerror	Keep browser open if script encountered an error

EXAMPLE:

cd bin
validator example-script.js

EXAMPLE:

cd bin
validator -browser FF example-script.js

In order to perform the validation procedure you must have Firefox installed.

If you wish to specify a particular location for the Firefox executable you may do so by creating a "config.properties" file containing the following entry:

FF3=/ff/firefox.exe

Where "/ff/firefox.exe" is an absolute pathname to the Firefox executable you wish to use for the validation process.

The "config.properties" file is commonly located in the ".wpm" directory under your user directory.

On Windows XP/2003 this location defaults to:

C:\Documents and Settings\<username>\.wpm

Under Windows Vista/7 this location defaults to:

C:\Users\<username>\.wpm

Please refer to the Neustar Web Performance Monitoring site for further assistance:  https://tools.wpm.neustar.biz/

