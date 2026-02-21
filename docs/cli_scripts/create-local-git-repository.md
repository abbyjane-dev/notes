# Create local git repository

*2025-12-10*

## Create function

``` bash
set -U GIT_HOME_<name of repository> "/Users/abby/Library/Mobile\ Documents/com~apple~CloudDocs/Programming/.git/.<name of repository>

funced --save <name of repository>

function <name of repository> --description 'Git for <reository>'
    /usr/bin/git --git-dir=$GIT_HOME_<NAME OF REPOSITORY>/.git --work-tree=<directory with files for repository> $argv
end
```

## Create local repository

> \*\*Note:\*\*For ease: name ofrepository = repotest</name>

``` bash
repotest init $GIT_HOME_REPOTEST'
```

## Create remote repository

``` bash
gh repo create

? What would you like to do?  [Use arrows to move, type to filter]
> Create a new repository on GitHub from scratch
  Create a new repository on GitHub from a template repository
  Push an existing local repository to GitHub

? Repository name repotest

? Description Place for tests

? Visibility  [Use arrows to move, type to filter]
  Public
> Private
  Internal

? Would you like to add a README file? (y/N) N

? Would you like to add a README file? No

? Would you like to add a .gitignore? No

? Would you like to add a license? No

? This will create "repotest" as a private repository on GitHub. Continue? (Y/n) Y
✓ Created repository abby/testrepo on GitHub
  https://github.com/abby/testrepo

? Clone the new repository locally? No
```

### Configure files to track

``` bash
testrepo config --local status.showUntrackedFiles no

cd <directory with files for repository>
```

```
repotest add <directories or files>
```

***Examples:***

`testrepo add test1/`  
\--Adds entire directory and subdirectories

`testrepo add test1/*.txt`  
\--Adds only the .txt files in that directory

`testrepo add $(find test1/test2/ -type f -maxdepth 1)`  
\--Adds only the files in test1/test2 directory without adding any files from test1/test2/test3 subdirectory

### Commit files

``` bash
testrepo commit -m "<Description of commit>"
```

### Configure push and push files

``` bash
testrepo remote add origin <url to repo created earlier>

testrepo branch -M main

testrepo push -u origin main
```

### Check status of local repository

``` bash
testrepo status
```