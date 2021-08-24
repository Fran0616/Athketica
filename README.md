# Athketica
In this project, you’ll use the commands you just learned to redirect files in Athletica, a sporting events directory.

Redirecting Input and Output
=

Redirection is a feature in Linux such that when executing a command, you can change  the stadard input/output devices. The basic workflow of any Linux command is that it takes an input and give an output. It is similar but different from pipes, as it allows reading/writting from files instead of only commands. Redirecting can be done by using the operators `>` `>>`. 
- The stadard input (stdin) device is the keyboard.
- The standard output (stdout) device is the screen. 



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
3
```
$ cat basketball.txt
Basketball is a sport played by two teams of five players on a rectangular court. Src: Wikipedia
```
4

```
$ cat hockey.txt
Basketball is a sport played by two teams of five players on a rectangular court. Src: Wikipedia
```

5
```
$ cat basketball.txt > hockey.txt
$ cat hockey.txt 
Basketball is a sport played by two teams of five players on a rectangular court. Src: Wikipedia

```
6

```
cat lacrosse.txt
Lacrosse is a contact team sport played between two teams using a small rubber ball and a long-handled stick called a crosse or lacrosse stick. Src: Wikipedia
```

7
```
$ cat lacrosse.txt >> tennis.txt 
$ cat tennis.txt 
Tennis is a racket sport that can be played individually against a single opponent (singles) or between two teams of two players each (doubles). Src: Wikipedia
Lacrosse is a contact team sport played between two teams using a small rubber ball and a long-handled stick called a crosse or lacrosse stick. Src: Wikipedia
Lacrosse is a contact team sport played between two teams using a small rubber ball and a long-handled stick called a crosse or lacrosse stick. Src: Wikipedia

```
8

```
$ cat < gymnastics.txt 
Gymnastics is a sport involving the performance of exercises requiring strength, flexibility, balance and control. Src: Wikipedia
```

9 
```
$ cat lacrosse.txt | wc
      1      27     159

```

10 

```
$ cat equipment.txt 
baseball
shuttlecock
shuttlecock
helmet
football
cleats
cleats
cleats
tennis ball
baseball bat
lacrosse stick
hockey stick
hockey stick
hockey stick
tennis racket
cricket bat
cricket bat
cricket bat
goggles
googles
swimming cap
lacrosse ball
hockey puck
sneakers
sneakers
skates
skates
skates
shinguards
$ 

```

11
```
$ sort equipment.txt
baseball
baseball bat
cleats
cleats
cleats
cricket bat
cricket bat
cricket bat
football
goggles
googles
helmet
hockey puck
hockey stick
hockey stick
hockey stick
lacrosse ball
lacrosse stick
shinguards
shuttlecock
shuttlecock
skates
skates
skates
sneakers
sneakers
swimming cap
tennis ball
tennis racket
```

12 
```
$ uniq equipment.txt 
baseball
shuttlecock
helmet
football
cleats
tennis ball
baseball bat
lacrosse stick
hockey stick
tennis racket
cricket bat
goggles
googles
swimming cap
lacrosse ball
hockey puck
sneakers
skates
```

13
```
$ grep Japan roster.txt
Yuki Hayashi, Swimming: Japan
Misako Sato, Gymnastics: Japan
Takumi Fujiwara, Basketball: Japan
Toshi Ogawa, Badminton: Japan
```

14 

```
$ grep -R player
basketball.txt:Basketball is a sport played by two teams of five players on a rectangular court. Src: Wikipedia
cricket.txt:Cricket is a bat-and-ball game played between two teams of 11 players each on a field at the centre of which is a rectangular 22-yard-long pitch. Src: Wikipedia
hockey.txt:Basketball is a sport played by two teams of five players on a rectangular court. Src: Wikipedia
tennis.txt:Tennis is a racket sport that can be played individually against a single opponent (singles) or between two teams of two players each (doubles). Src: Wikipedia
```

15 
```
$ sed 's/loss/win/g' games.txt
Australia vs United Kingdom
Australia: win

United States vs South Africa
United States: win

Mexico vs Colombia
Colombia: win

Brazil vs Argentina
Brazil: win

Kenya vs Ghana
Kenya: win

Jordan vs Morocco
Morocco: win

Malaysia vs Singapore
Singapore: win

India vs China
India: win

Pakistan vs Uzbekistan
Uzbekistan: win

Greece vs Turkey
Greece: win

France vs Spain
France: win$ 

```

Cheetsheet
= 

Redirecting Output

The `>` symbol is used to redirect output by taking the output from the command on the left and passing as input to the file on the right.

```
cho "Hello" > hello.txt
```
cat Display

The shell command cat displays the contents of one or more files to the terminal.

```
$ cat poem.txt
$ cat poem.txt kitties.txt
```

Append Redirect shell command

The `>>` shell command is used to redirect the standard output of the command on the left and append (add) it to the end of the file on the right.

```

# This command will append "Hello World!" to greetings.txt
echo "Hello World!" >> greetings.txt
```
Pipe shell command

The `|` command is called a pipe. It is used to pipe, or transfer, the standard output from the command on its left into the standard input of the command on its right.

```
# First, echo "Hello World" will send Hello World to the standard output.
# Next, pipe | will transfer the standard output to the next command's standard input.
# Finally, wc -w will count the number of words from its standard input, which is 2.
echo "Hello World" | wc -w
```

grep Search

The shell command `grep` is used to search files for lines that match a pattern and returns the results. Various options can be specified along with the `grep` command to specify the search.

In the provided example, the lines in the file names.txt which contain “sonny” will be returned.

```
grep 'sonny' names.txt
```

Case insensitive search

The shell `grep` command searches files for a particular pattern. The `grep` command with the `-i` option can be used to search files for lines that match a pattern, case insensitive, and returns the results.

grep -R shell command

The shell command `grep` has a `-R` option (`grep -R`) that searches all files in a directory, including its subdirectories, and outputs filenames and lines containing matched results.
