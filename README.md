# Core
Core module for CryHavok's malware elimination suite

## Purpose
The core module will expose the basic functionality and engine for creating 'prescriptions' for eliminating 'infections' (ie,  malware and other dangerous, unethical and unwanted software and configuration found on a system. )

> This Project is not simply satisfied to classify 'infections' as simply viruses or deliberate malware, but to also seek out and destroy any software that violates the user's trust (ie, introduces privacy issues, leaks data, uses questionable practices to diminish the user's security, safety or stability, etc)

## Ideas:
 - a scriptable set of tools that can allow users to find and maniupulate 'infections'
 - a set of library functions for doing the low-level grunt-work
 - could also be used to make an open, scriptable and extensible 'CCleaner' clone. Without the closed-source mystery.
 - focus on collaboration and simplicty so that as many users as possible can share their 'prescriptions' and have them peer evaluated 

## Basic Functionality

These include the following parts of the functionality:

### Find Target
  the functionality that can find active or inactive 'infections' and their related files, settings, registry keys, certificates, etc.

### Isolate Target
  the functionality that can disable and isolate (without initially killing) a given 'infection'. Often, malware will try to restart itself before allowing itself to be killed. This functionality will inhibit a peice of software from continuing without causing it to get defensive.
  
### Terminate Target
  the functionality to kill a process (or set of processes) that are related to an 'infection'. Some malware has defenses against this sort of thing, so this will include a set of increasingly powerfull task-stopping functions. 

### Delete Target
  Permanently removing such files is far-too-often difficult because of locked files, hard to tweak permissions, etc. I've got a large bag of tricks that I can use to aggressively eliminate such files, and it's time that I make this easy to do.

### Share Perscriptions
  We also need to be able to post, share and validate 'perscriptions' so that they can be easily applied to any system. These 'perscriptions' should be able to run sufficently fast to identify 'infections' so that we can eventually setup ongoing monitoring of a system as a preventative measure.
  
## Implementation Thoughts
- ProcessHacker (http://processhacker.sourceforge.net/) is an open-source tool that contains a huge amount of low-level functionality that will be necessary to find, immobilize and terminate 'infections'. I think I'd like to fork that, remove the UI and turn it into a general purpose library that we can leverage so that we're not reinventing the wheel.
- I'm leaning towards using PowerShell as the scripting engine (and/or possibly leveraging the OneGet plugin engine), since we can start by simply exposing ProcessHacker functionality to PowerShell, and using PowerShell modules as the 'perscription' language gives us a ton of flexibility without having to do much work.
- as we go, we can add more complicated search functionality and new scripts can leverage them right away.
- I suspect that the fastest means to share perscriptions could be done leveraging github and/or github gists. 
