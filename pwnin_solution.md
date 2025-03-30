# PIE TIME Writeup - picoCTF

**Challenge Name**: PIE TIME  
**Category**: Binary Exploitation  
**Difficulty**: Easy  
**Points**: 200  
**Tools Used**: 
- `file`
- `gdb`
- `objdump`
- `nc`

## Challenge Description
> Can you exploit this binary to get the flag? The binary has PIE enabled, but you have the source code.
> Connect with: `nc rescued-float.picoctf.net 63140`

## Step 1: Initial Setup
1. Launched the challenge instance on picoCTF
2. Downloaded:
   - Binary: `vuln`
   - Source code: `vuln.c`

## Step 2: Binary Analysis
### Basic Reconnaissance
```bash
$ file vuln
vuln: ELF 32-bit LSB executable, Intel 80386, dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=..., for GNU/Linux 3.2.0, not stripped

## Step 3:Dynamic Analysis with GDB

## Opened binary in GDB:\

$ gdb vuln

## Found critical addresses:

(gdb) disass main

(gdb) disass win

## calculated difference by calculator, and then converted into hexadecimal

## Step 4: Exploitation

## Connected to the service:

$ nc rescued-float.picoctf.net 63140

## Got the flag
