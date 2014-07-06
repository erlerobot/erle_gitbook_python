## Exercises: File Input /Output

######Exercise 1
Write a program to prompt for a file name, and then read through the file line-by-line.
Note: the file name is `Erle.txt`and its content is,
```
Erle is the enabling technology for the
next generation of aerial and terrestrial
robots that will be used in cities solving
tasks such as surveillance, enviromental
monitoring or even providing aid at catastrophes.
```
Ensure you create the file.

######Exercise 2
Create a file called `new_world.txt`.First add a new line to the file:`Welcome to robotics time.`. And then print the content of `new_world.txt`.

##Solutions

######Exercise 1

The solution code is the following:
```
  name=raw_input("Enter the file name:")

  my_file=open(name,"r")

  print my_file.readline()
  print my_file.readline()
  print my_file.readline()
  print my_file.readline()


 my_file.close
 ```

 Store this in `e_py.py`file. The result of the execution is:
 ```
 root@erlerobot:~/Python_files# python e_py.py
Enter the file name:Erle.txt
Erle is the enabling technology for the

next generation of aerial and terrestrial

robots that will be used in cities solving

tasks such as surveillance, enviromental

root@erlerobot:~/Python_files#
```

######Exericse 2
The code should be stored on `nworld.py`and then executed:
```
 my_file=open("new_world.txt","r+")

 line= "Welcome to robotics time."
 my_file.write(line)

 print  my_file.read()

 my_file.close()
 ```

```
root@erlerobot:~/Python_files# python nworld.py
Welcome to robotics time.
```
