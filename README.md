#Shell script Linux - "chrdpass"

##Description
'chrdpass' is a shell script that can help you with below three purposes :

- Change password of user in Linux with strong random string then print out password on terminal for you.
- Change password of user in Linux with strong random string has a specific length of string.
- Change password of user with password that user want to use.
- Default max length of random string is 12 characters.
- Script create random string with the natural calculation, does not depend on any tool to create random pass.


##Requirements

- Tool 'chpasswd' need to be installed on Linux. Default Linux has it.
- Privileges to run 'chpasswd' like root.
- Git command on system.

##Installation

**+ Linux**

```sh
# git clone https://github.com/cuongquach/chrdpass-linux.git chrdpass
# mv chrdpass/chrdpass.sh /usr/bin/
# chmod 700 /usr/bin/chrdpass && chown root:root /usr/bin/chrdpass
# which chrdpass
/usr/bin/chrdpass
```

##Example Usage
###Options

- **-u** : assign the name of user in Linux system that you want to change password. Script has function to check that user is avaiable or not.
- **-m** : assign the number indicates max length of random password that script can generate in time. Default is : **12** .
- **-p** : assign password input that sysadmin want to use instead of using random password from script.

###Notice
- The range of random password's max length is avaiable between 7 and 35 .
- Do not use option **[-m]** with option **[-p]** .
- Do not use 

##Author
**Name** : Quach Chi Cuong

**Website** : https://cuongquach.com/

