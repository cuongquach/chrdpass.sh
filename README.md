#Shell script Linux - "chrdpass"

##Description
'chrdpass' is a shell script that can help you with below three purposes :

- Change password of user in Linux with strong random string then print out password on terminal for you.
- Change password of user in Linux with strong random string has a specific length of string.
- Change password of user with password that user want to use.

Default max length of random password is 12 characters.

Script create random string with the natural logic calculation, does not depend on any tool to create random pass.

Password will be encrypted with the algorithm SHA512 instead of MD5 which is default in Linux.


##Requirements

- Tool 'chpasswd' need to be installed on Linux. Default Linux has it.
- Privileges to run 'chpasswd' like root.
- Git command on system.

##Installation

**+ Linux**

```sh
$ git clone https://github.com/cuongquach/chrdpass-linux.git chrdpass
$ mv chrdpass/chrdpass.sh /usr/bin/
$ chmod 700 /usr/bin/chrdpass && chown root:root /usr/bin/chrdpass
$ which chrdpass
/usr/bin/chrdpass
```

##Example Usage
### Examples
**Ex 1** : change password of a user with generated random pass.

```sh
$ chrdpass -u demo
User : demo
New pass: XVSGAg1ioBPF
- Change password for user [demo]  SUCCESS. Exit
```

**Ex 2** : change password of a user with generated random pass that has a specific max length.

```sh
$ chrdpass -u demo -m 25
User : demo
New pass: dy4eNJCh6IP3y0i4dh148qsuh
- Change password for user [demo]  SUCCESS. Exit
```


**Ex 3** : change password of a user with a string that user provide to script.

```sh
$ chrdpass -u demo -p secretpass
User : demo
New pass: secretpass
- Change password for user [secretpass]  SUCCESS. Exit
```

**Ex 4** : get the help page.

```sh
$ chrdpass -h
Usage : 
	   /usr/bin/chrdpass [-h] [-u] <agrument1> [-p] <agrument2> [-m] <agrument3>

Option :
        -u 	username of user in system that you want to change password.
        -p 	the password input from user. If you dont want to user RANDOM password which created by \"0\"
        -m 	max length of Random password which created by \"/usr/bin/chrdpass\"
        -h 	help page

Notice :
        - You have to specific the user [-u] in agrument of command.
        - Use option user [-u] only if you want to change password with RANDOM String.
        - Default max length [-m] is 12.
        - Option max length [-m] just use with option user [-u].
        - Never use option password [-p] with [-m].
        - Never use password [-p] with the length of it is shorter than 7 or greater than 35.

Examples : 
        $ /usr/bin/chrdpass -u demo1
        $ /usr/bin/chrdpass -u demo1 -m 15
        $ /usr/bin/chrdpass -u demo2 -p secretpass
```

 

####Options

- **-u** : assign the name of user in Linux system that you want to change password. Script has function to check that user is avaiable or not.
- **-m** : assign the number indicates max length of random password that script can generate in time. Default is : **12** .
- **-p** : assign password input that sysadmin want to use instead of using random password from script.

####Notice
- The range of random password's max length is avaiable between 7 and 35 .
- Do not use option **[-m]** with option **[-p]** .
- Do not use 

##Author
**Name** : Quach Chi Cuong

**Website** : https://cuongquach.com/
