All Git Commands that I know

## Set commands

### Environment
        1. --system
        2. --global
        3. --local

## Config set commands
    1. git config --local user.name "Name_here"
    2. git config --global user.email "durgeshsinght2004@gmail.com"
    
## Config unset Commands
    1. git config --global --unset user.name
    2. git config --local --unset user.email
    3. git config --system --unset user.email

### git configuration cmds
    1. git config --global --list
    2. git config --list --global
    3. git config --list

## Repo Cloning cmd
    1. git clone link_here_without_any_Quotes

## File Adding& commit
    1. git add file_name_here_along_with_relative_position
	2. git add .
    3. git commit -m "message_here"

	
##	4 states of git files 
		1. Untracked
		2. Modified
		3. Staged
		4. Unchanged


## Status cmd
    1. git status

## Push cmd
    1. git push origin main

## git tag
	to show details of the perticular tags 
	1. git tag
	2. git show v1.1
	First commit changes, then add tag
	3. git tag -a v2.0 -m "Message"
	4. git show v1.1
	5. git push origin v2.0
## To show history
	1. git log --oneline
	2. git log
	3. git log <filename>
