# linux-command-line

## Linux
Linux is an operating system. In fact, one of the most popular OS on the planet. Linux is aa free. So many distrous of linux
- Ubuntu
- CentOS
- Debian
- Mint
- Red Hat
- Alpine
- Kali

![image](https://user-images.githubusercontent.com/85268263/150717837-49d68a44-e00c-45d6-9af0-10359f2be7f5.png)

## The CLI
command pwd for know where directory u run a command

```sm
yusuf@Yusufs-MacBook-Pro ~ % pwd
/Users/yusuf
```

command ls for know list file or folder in directory

```sm
yusuf@Yusufs-MacBook-Pro ~ % ls
Applications	Documents	Library		Music		Postman
Desktop		Downloads	Movies		Pictures	Public
```

command echo for print words

```sm
yusuf@Yusufs-MacBook-Pro ~ % echo "welcome to course yusuf"
welcome to course yusuf
```

command wich is tell u you program running

```sm
yusuf@Yusufs-MacBook-Pro ~ % which ls
/bin/ls
```

## Editor

### nano
nano is an old open source text editor that itself was an evolution from a previous text editor called pico. Pico was the text editor of the command-line email client Pine that people grew to love so much that they used it for everything. Because Pine was licensed in such a way that Debian wouldn't include it with its distro, Chris Allegretta re-implemented under the name TIP (Tip Isn't Pico, computer scientists love recursive acronyms) it eventually was renamed to nano.

Due its tiny size, light weight, and permissive license, nano is included on just about every Linux/Unix-like OS and is frequently the default text editor, even on tiny little embedded devices where even vim is too much. As such, it's a good tool to have your tool belt if you need to do some light text editing.
![GitHub Light](https://btholt.github.io/complete-intro-to-linux-and-the-cli/static/7c2c5569f855f6137bba414f9577cd48/afa26/nano.png)
### vim
The genesis of the ideas that went into vim started with an editor called ed (said ee-dee) which itself was inspired by a previous editor called qed. ed was developed by Ken Thompson at Bell Labs in 1969. It is a line-oriented editor and I have no clue how to use it. It's actually rather well known for being pretty user unfriendly. In spite of this, it's still available on most Unix-like systems including Ubuntu and macOS. If you do start it, just know it's CTRL+D a few times to quit it. It's important to note that ed was created in a time where memory was precious, screens were tiny and sometimes just one line at a time, and modems were measured in bits, not even kilobits. It arose at a time when it fit its constraints.

vim has multiple modes you can put the editor into. By default we are in command mode. So if you start typing, nothing will appear and you may actually accidentally trigger some commands. If you want to kick the editor into insert mode, just hit `i`. You should see `-- INSERT --` at the bottom to let you know you can type now. I'm going to put `vim test`. at the bottom of the file. Once I'm done writing and want to head back to command mode, you can hit Esc. You'll see the `-- INSERT --` disappear.

vim has an absolute myriad of commands and I'm not going to get into it. A good example is that here in command mode, you can use H to move the cursor left, j goes down, k goes up, and l goes right (the arrow keys work too but vim masters try to not take their fingers off the home row keys.) If I highlight a character and hit x, it'll delete that character. If I move my cursor to a line and type `:d` it'll delete the whole line. If I type `:d3` it'll delete three lines. There are so, so many and you just have to learn them.

If you do desire to go in-depth on vim, you can do one of two things. One is to type `:help tutor` from the command mode and it'll start the tutor. A more fun way is vim adventures which is a fun game to learn the keys.
![GitHub Light](https://s.yimg.com/uu/api/res/1.2/FHOZT3ho7HV7HJiqnOO85w--~B/Zmk9ZmlsbDtoPTQ0MTt3PTY3NTthcHBpZD15dGFjaHlvbg--/https://s.yimg.com/uu/api/res/1.2/BFH48vOvKgtQpO7v.IDCSA--~B/aD0zOTI7dz02MDA7YXBwaWQ9eXRhY2h5b24-/https://www.blogcdn.com/www.engadget.com/media/2012/06/vimtitle.jpg.cf.webp)

## Files

### Reading file
```sm
yusuf@Yusufs-MacBook-Pro ~ % less textfile.txt

coba text terserah
textfile.txt (END)
```

### Creating Folder

```sm
yusuf@Yusufs-MacBook-Pro ~ % mkdir yusuf-new-folder
yusuf@Yusufs-MacBook-Pro ~ % ls
Applications		Library			Postman
Desktop			Movies			Public
Documents		Music			textfile.txt
Downloads		Pictures		yusuf-new-folder
```

### Create new File

```sm
yusuf@Yusufs-MacBook-Pro ~ % touch my-new-file.txt
yusuf@Yusufs-MacBook-Pro ~ % ls
Applications		Movies			my-new-file.txt
Desktop			Music			textfile.txt
Documents		Pictures		yusuf-new-folder
Downloads		Postman
Library			Public
```

### Delete file

```sm
yusuf@Yusufs-MacBook-Pro ~ % rm my-new-file.txt
yusuf@Yusufs-MacBook-Pro ~ % ls
Applications		Library			Postman
Desktop			Movies			Public
Documents		Music			textfile.txt
Downloads		Pictures		yusuf-new-folder
```

### Copy file

```sm
yusuf@Yusufs-MacBook-Pro ~ % cp textfile.txt destination.txt
yusuf@Yusufs-MacBook-Pro ~ % ls
Applications		Movies			destination.txt
Desktop			Music			textfile.txt
Documents		Pictures		yusuf-new-folder
Downloads		Postman
Library			Public
yusuf@Yusufs-MacBook-Pro ~ % less destination.txt

coba text terserah
destination.txt (END)

```

## Environment

Whether or not you realize it, your current session of your shell has a bunch of variables set. Most are just set by the OS, some by Multipass (or whatever you're using to run your computer), some by various programs, and some by you.

```sm
yusuf@Yusufs-MacBook-Pro ~ % printenv
__CFBundleIdentifier=com.apple.Terminal
TMPDIR=/var/folders/g9/njwv9m9d7_gbwd2bczt1jl7r0000gn/T/
XPC_FLAGS=0x0
LaunchInstanceID=06B5CA7D-7C03-494C-8A00-93C289A50FA7
TERM=xterm-256color
SSH_AUTH_SOCK=/private/tmp/com.apple.launchd.ZGFllJ8Pnf/Listeners
SECURITYSESSIONID=186a5
XPC_SERVICE_NAME=0
TERM_PROGRAM=Apple_Terminal
TERM_PROGRAM_VERSION=440
TERM_SESSION_ID=5F909BC4-1B97-4525-9741-2F75E9D0157F
SHELL=/bin/zsh
HOME=/Users/yusuf
LOGNAME=yusuf
USER=yusuf
PATH=/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/opt/homebrew/bin
SHLVL=1
PWD=/Users/yusuf
OLDPWD=/Users/yusuf
LC_CTYPE=UTF-8
_=/usr/bin/printenv

yusuf@Yusufs-MacBook-Pro ~ % echo $USER
yusuf
```

## Process
At all times with Linux a certain amount of processes will be running. A process is any sort of command that's currently running. For example, if you have a shell open, you're running bash as a process.

```sm
yusuf@Yusufs-MacBook-Pro ~ % ps
  PID TTY           TIME CMD
  619 ttys000    0:00.04 /bin/zsh -l
 5962 ttys000    0:14.13 node /opt/homebrew/Cellar/yarn/1.22.11/libexec/bin/yar
 5963 ttys000    0:00.11 /usr/local/bin/node /Users/yusuf/Documents/Project/new
 5967 ttys000    1:27.79 /usr/local/bin/node server
23720 ttys001    0:00.13 -zsh
21457 ttys002    0:00.03 /bin/zsh -l
```
## Script
Often times you want do more than just one command at a time; you want to run many of them. Bash allows you to put many commands into one file to create a program of programs which is called a shell script.

```sm
yusuf@Yusufs-MacBook-Pro ~ % vi gen_files.sh

mkdir -p ~/temp
cd ~/temp
touch file{1..10}.txt
echo done

yusuf@Yusufs-MacBook-Pro ~ % source gen_files.sh
done

yusuf@Yusufs-MacBook-Pro temp % cd ~/temp
yusuf@Yusufs-MacBook-Pro temp % ls
file1.txt	file2.txt	file4.txt	file6.txt	file8.txt
file10.txt	file3.txt	file5.txt	file7.txt	file9.txt
```


##Resource
* https://btholt.github.io/complete-intro-to-linux-and-the-cli

