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
  Permanently removing such files is far-too-often 

### Share Perscriptions
