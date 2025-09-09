# Lab 02

- Name:Utsav Acharya 
- Email: acharya.41@wright.edu

## Part 1 Answers

Full / absolute path to your private key file: /mnt/c/Users/User/Desktop/labsuser.pem


Command to SSH to AWS instance:
```
ssh -i /mnt/c/Users/User/Desktop/labsuser.pem ubuntu@54.157.67.102

```

## Part 2 Answers

1. `chmod u+r bubbles.txt`
    - Means: gives permisssion for the user on bubbles.txt
    - Assessment:if user has not permisssion now user can open and read the file . 
2. `chmod u=rw,g-w,o-x banana.cabana`
    - Means: give user permission to read and write , remove write permisssion from group , removes execute from others.
    - Assessment:user can read and edit the file. group can still read but  not write  where others can't execute file.
3. `chmod a=w snow.md`
    - Means: set all users write only permission.
    - Assessment:Everyone can modify the file, but no one (not even the owner) can read or execute it.
4. `chmod 751 program`
    - Means: User has full permissions (rwx = 7), group has read + execute (5), others have execute only (1).
    - Assessment:he file owner can do everything. Group can run the program and view contents. Others can only run it, not view or edit.
5. `chmod -R ug+w share`
    - Means: Recursively grants write permission to user and group for the directory share and file and subfolder with in it .
    - Assessment:Ensures user and group can create, modify, and delete files inside share.

## Part 3 Answers

1. Command to create new user: sudo useradd joker
2. Path to new user's home directory: /home/joker
3. Evaluate if `ubuntu` can add files to new user's home directory: No the permission change is required
4. Command to switch to new user: sudo su joker
5. Command(s) to go to new user's home directory:cd /home/joker
6. Evaluate if new user can add files to user's home directory: No
7. Command to return to `ubuntu` user:sudo su -ubuntu
8. Command to return to `ubuntu` home directory: cd/home/ubuntu

## Part 4 Answers

1. Command(s) to create group named `squad` and add members:sudo groupadd squad
2. Command(s) to add `ubuntu` & user to group `squad`:
sudo usermod -aG squad ubuntu
sudo usermod -aG squad joker
3. Command(s) to allow `squad` to view the `ubuntu` user's home directory contents:
sudo chmod 750 /home/ubuntu
sudo chgrp squad /home/ubuntu
4. Command(s) to modify `share` to have group ownership of `squad`:sudo chown :squad changrp -R squad share

7. Describe your tests and commands with the user account: 

Switched to joker: su - joker

Navigated to /home/ubuntu/share → verified access.

Created a file inside → touch text.txt.

7. Describe the full set of permissions / settings that enable the user to make edits:
Directory share owned by group squad.

Group squad has write permissions.

Both ubuntu and joker are members of squad.

## Part 5 Answers

For each, write the command used or answer the question posed.

1. Command(s) to make file using `sudo`: sudo touch ilovemeat.txt
2. Command(s) to make file with `root`:
 sudo su

touch ilovemeat.txt

exit

4. Describe / compare ownership and permissions of files:
 Files created with sudo or root are owned by root:root.

Files created with a normal user are owned by username:username.

Permissions default to rw-r--r-- unless changed.

5. Which account can do what actions? (Type Y or N in columns)

Contents inside of `share`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    |  Y         |   Y        |           Y                |
| `ubuntu`  |   Y        |    Y       |            N
| `BOB`     |    Y       |  Y         |             N              |

`madewithsudo.txt`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    |   Y        |    Y       |                 Y          |
| `ubuntu`  |    Y       |     N      |                  N         |
| `BOB`     |     Y      |      N     |                   N        |

5. Command(s) to modify permissions:
chmod 664 madewithsudo.txt
   
chown ubuntu:squad madewithsudo.txt
7. How to give user account `sudo`:
sudo usermod -aG sudo joker
## Citations
AWS Academy Learner Lab instructions (course module)

LAB TA 


CLASS TEACHER BIBECK 

LINUX MAN PAGES 

I USED CHATGPT FOR FIND THE SSH TO AWS UBUNTU user name
