# Athketica
In this project, you’ll use the commands you just learned to redirect files in Athletica, a sporting events directory.

Task 
=

1. Print the working directory
2. List all the files and directories in long format, including hidden files.
3. Use `cat` to view the contents of basketball.txt
4. Use `cat` to view the content of hockey.txy
5. Redirect the stadard output of basketball.txt into hockey.txt Then view the contents of hockey.txt
6. View the contents of lacrosses.txt 
7. Append the contennts of lacrosse.txt to the contents of tennis.txt Then view the contents of tennis.txt
8. Redirect the contents of gymnastics.txt as stadard input for the `cat` command. 
9. Pipe the standard output of `cat laccrosse.txt` to the wordcount command. 
10. Use `cat` to view the contents of equipment.txt.
11. Sort the contents of equipment.txt in alphabetical order. 
12. Use the `uniq` command to filter out adjacent, duplicate lines in equipment.txt
13. Use `grep` command to search roseter.txt for players from Japan. 
14. Use the `grep` command to search for the string 'player' in the current directories(`.`), and output filenames and lines for matched results.
15. Use `cat` to view the contents of games.txt. Then, use `sed` to replaces all instances of words 'loss' with 'win' in games.txt


Task Input/Output
=
1
```
$ pwd
/home/ccuser/workspace/athletica
```
2 

```
$ ls -la
total 56
drwxr-xr-x 2 ccuser ccuser  259 Aug 24 01:48 .
drwxrwxr-x 1 ccuser ccuser   23 Aug 24 01:48 ..
-rw-r--r-- 1 ccuser ccuser  102 Aug 24 01:48 badminton.txt
-rw-r--r-- 1 ccuser ccuser   97 Aug 24 01:48 basketball.txt
-rw-r--r-- 1 ccuser ccuser  161 Aug 24 01:48 cricket.txt
-rw-r--r-- 1 ccuser ccuser 6148 Mar  5  2016 .DS_Store
-rw-r--r-- 1 ccuser ccuser  304 Aug 24 01:48 equipment.txt
-rw-r--r-- 1 ccuser ccuser  117 Aug 24 01:48 football.txt
-rw-r--r-- 1 ccuser ccuser  393 Aug 24 01:48 games.txt
-rw-r--r-- 1 ccuser ccuser  130 Aug 24 01:48 gymnastics.txt
-rw-r--r-- 1 ccuser ccuser   97 Aug 24 01:50 hockey.txt
-rw-r--r-- 1 ccuser ccuser  159 Aug 24 01:48 lacrosse.txt
-rw-r--r-- 1 ccuser ccuser  605 Aug 24 01:48 roster.txt
-rw-r--r-- 1 ccuser ccuser   69 Aug 24 01:48 swimming.txt
-rw-r--r-- 1 ccuser ccuser  319 Aug 24 01:52 tennis.txt
$ 
```
