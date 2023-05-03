OverTheWire - bandit

https://overthewire.org/wargames/bandit/

Level 0

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.
![image](https://user-images.githubusercontent.com/110773559/235846017-edb4b70c-915b-4e07-8480-15fa9eddee15.png)


Level 0 -> Level 1

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
I used the ‘ls’ command to view all the files list and ‘cat’ to execute all the information from the file. 
![image](https://user-images.githubusercontent.com/110773559/235846116-5eed15d5-9c50-45ea-95d2-d823e4571aad.png)

Now, from here type ‘exit’ and SSH back into the next level by running
![image](https://user-images.githubusercontent.com/110773559/235846201-f017d2d9-76f2-4007-93f0-879b6c3ea2b0.png)


And I'm in!

![image](https://user-images.githubusercontent.com/110773559/235846259-7fd759ba-ba3b-48ca-ab25-71a0f3bb6304.png)


Level 1 -> Level 2
The password for the next level is stored in a file called - located in the home directory
![image](https://user-images.githubusercontent.com/110773559/235846337-d176ae64-46bf-492c-8bfe-05ab2fc1b224.png)

As in the previous level, we ssh to the next user (bandit2) with the given password.
Level 2 -> Level 3

The password for the next level is stored in a file called spaces in this filename located in the home directory
![image](https://user-images.githubusercontent.com/110773559/235846462-e091de07-a236-4e8b-93a7-63a37e2a6f2e.png)

Now we ssh to bandit3 with this password
![image](https://user-images.githubusercontent.com/110773559/235846532-74d9016f-48cd-4583-a4ea-c50b4a65c7a0.png)


We are in (:
Level 3 -> Level 4

The password for the next level is stored in a hidden file in the inhere directory.

![image](https://user-images.githubusercontent.com/110773559/235846615-38af6d86-0ccc-41bc-8347-2ac003bd3678.png)


And now we ssh to the next user 
![image](https://user-images.githubusercontent.com/110773559/235846689-5c531fd9-d45d-4b9f-b17b-03ab267bad80.png)


Level 4 -> Level 5
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
![image](https://user-images.githubusercontent.com/110773559/235846754-1191aeb8-594f-4ef2-964d-bd73c97436b0.png)


I figured out what type of file each one of them (because of the hint) 
![image](https://user-images.githubusercontent.com/110773559/235846853-92abe621-9c01-45cd-8eec-a62077558e9a.png)


And I already solved the challenge


Level 5 -> Level 6
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
human-readable
1033 bytes in size
not executable
![image](https://user-images.githubusercontent.com/110773559/235846947-201af1cf-2b8f-4da3-9d89-531b45e1f252.png)


And we solved it! 

![image](https://user-images.githubusercontent.com/110773559/235847028-43c1e604-10b1-4d5b-be7a-9511094403d0.png)

Level 6 -> Level 7
The password for the next level is stored somewhere on the server and has all of the following properties:
owned by user bandit7
owned by group bandit6
33 bytes in size
![image](https://user-images.githubusercontent.com/110773559/235847094-1a791801-99e1-4b9b-9a8d-322e4acbeb25.png)


And I found:
![image](https://user-images.githubusercontent.com/110773559/235847159-74313e30-b20e-431c-bad8-fffeb127abb2.png)

And here is the password:
![image](https://user-images.githubusercontent.com/110773559/235847232-2ecd4ed9-32fd-4bab-9aac-7c923cdad6a8.png)

Level 7 -> Level 8
The password for the next level is stored in the file data.txt next to the word millionth
I checked the current directory
![image](https://user-images.githubusercontent.com/110773559/235847299-99324271-df74-4529-a6d0-4dd789af0c42.png)

I used ‘strings’ and ‘grep’ commands to view the password.  
![image](https://user-images.githubusercontent.com/110773559/235847343-996571c8-f88f-4ca9-ae67-d95314ab76ba.png)

Level 8 -> Level 9
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
![image](https://user-images.githubusercontent.com/110773559/235847401-e68ecdd2-c961-4d4f-a128-31e01477f707.png)

Level 9 -> Level 10
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
![image](https://user-images.githubusercontent.com/110773559/235847440-20aba5ea-f0c4-40d3-8be7-9545dce2d941.png)

The password for the next level is stored in the file data.txt, which contains base64 encoded data
![image](https://user-images.githubusercontent.com/110773559/235847567-05bcdd34-0468-4537-8b73-c24bd420d2ab.png)

Level 10 -> Level 11
The password for the next level is stored in the file data.txt, which contains base64 encoded data

Level 11 -> Level 12
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions



Level 12 -> Level 13
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
As mentioned in the question make a new directory in /tmp and rename the file.















‘xxd’ program is used to make a hexdump or to do the reverse. Option -r convert hexdump into the binary. File file.txt is a hexdump and convert into a binary file file1.bin using the command

Using command file file1.bin, we found that file1.bin is a gzip compressed data. 
‘zcat’ is a program supplied with gzip and is used to decompress gzip-compressed files.

Again using the file command on file2, we found that it is bzip2 compressed data. ‘bzcat’ program is supplied with bzip2 and is used to decompress bzip2 compressed files.

file3 is gzip compressed file so use the ‘zcat’ program to decompress it in file4. file4 is a POSIX tar archive.
‘tar’ program is used for archiving files and options x is used to extract an archive, f is used to specify the name of the tar archive, and v is used for a more detailed listing.

Level 13 -> Level 14
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on













Level 14 -> Level 15
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

Level 15 -> Level 16
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.
Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section on the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…




Level 16 -> Level 17
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First, find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

I tried the port with the SSL - 31790

I created a folder named ‘abc’ and copied the RSA private key.



I used the chmod command to change the access premission of the file

I used the ssh command to continue the next level

And we are in! 

Level 17 -> Level 18

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

And we see the ‘Byebye!’ when we tried to log in




Level 18 -> Level 19
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

Level 19 -> Level 20
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.


Level 20 -> Level 21
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
NOTE: Try connecting to your own network daemon to see if it works as you think
I ran ‘suconnect’ to figure out what it is:

I know now that ‘suconnect’ creates a connection so I opened another terminal tab with bandit20 to create a connection with Netcat (nc), I chose 32000 port randomly 



Then I connected to this port using USID binary on the original bandit20

I submitted my password for getting my password for the next level:


Level 21 -> Level 22
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Level 22 -> Level 23
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.
NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.


Level 23 -> Level 24
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in mks for the configuration and see what command is being executed.
NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!
NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

































