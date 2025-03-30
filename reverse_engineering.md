# FlagHunters Writeup - picoCTF

**Challenge Name**: FlagHunters  
**Category**: Reverse Engineering  
**Difficulty**: Easy  
**Points**: 100  
**Tools Used**: 
- `cat`
- Python interpreter

## Challenge Description
> Analyze this Python poetry reader to find the hidden flag.  
> Connect with: `nc <host> <port>`

## Step 1: Initial Analysis
### Source Code Review
```bash
$ cat lyrical-reader.py

## Step 2: Vulnerability Discovery

## Flag Location: Stored in initial lines of the poem

##Input Parsing:
##Splits input by semicolon (;)

##Checks for exact match: Crowd; RETURN 0

##Injection Point: Command injection through verse selection

## Step 3: Exploitation

## Connecting to server

$ nc verbal-sleep.picoctf.net 59898

## Sent crafted input:

Which verse do you want? Crowd; RETURN 0

## input ;RETURN 0

## Received output containing flag in initial lines
