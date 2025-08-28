# CEG-2350---OS-Concepts-and-Usage-Utsav_FALL_2025
Utsav Acharya 
## Lab 01

- Name:Utsav Acharya
- Email:acharya.41@wright.edu

## Part 1 - GitHub Profile

1. https://github.com/utasar)

## Part 2 - Research

| Windows | Linux / Mac | Action |
| ---     | ---         | ---    |
| help    | man         | to get help of the running command       |
| Get-Location | pwd    | to get the path location       |
| Get-ChildItem | ls    |   to list the file with in the directory or files     |
| mkdir   | mkdir       |   make      |
| Set-Location | cd     |        |
| New-Item | touch      |        |
| Move-Item | mv        |        |
| Copy-Item | cp        |        |
| Remove-Item | rm      |        |
| notepad.exe | vim     |        |

## Part 3 - Command Line Navigation

My OS is:
- [x] Windows
- [] Linux
- [] Mac

My Command Line Shell is: 
window power shell
### Navigating My OS on the Command Line

1. Full / absolute path to your user's home directory:
2. Create a directory named `DirA`: mkdir DirA
3. Create a directory named `Dir B`: mkdir Dir B
4. Go into `DirA`:Set-Location DirA
5. Go into `Dir B` from `DirA`: Set-location Utsav and Set-location DirB
6. Return to your user's home directory:CD ../..
7. Create a file named `test.txt`: mkdir test.txt
8. Move the file named `test.txt` into `DirA`:Move-item test.txt DirA
9. Contents of `test.txt`:cat test.txt
```
Put your words here 123333
```
10. Make a copy of `test.txt` named `copy.txt` in `DirA`:     copy test.txt DirA\copy.txt 
11. View the contents of `DirA`: vim DirA
12. Make a copy of `test.txt` in `Dir B` named `fodder.txt`:Copy-Item -Path "C:\Users\haede\DirA\test.txt" -Destination "C:\Users\haede\Dir B\fodder.txt"
Delete / remo
13. Delete / remove both `fodder.txt` AND `Dir B`:Remove-Item Dir B -Recurse

## Citations

To add citations, provide the site and a summary of what it assisted you with.  If generative AI was used, include which generative AI system was used and what prompt(s) you fed it.



