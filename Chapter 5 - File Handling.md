# Chapter 5 - File Handling

File handling in Python refers to the process of working with files on the computer's storage system. It involves tasks such as reading from files, writing to files, and manipulating file data. Python provides built-in functions and methods to perform file handling operations.

Opening a File:

To begin working with a file, you need to open it. The open() function is used to open a file and returns a file object that can be used for subsequent operations.

Here's an example of opening a file in read mode:
```
file = open("example.txt", "r")
```

In the above example, example.txt is the name of the file, and "r" is the mode indicating that the file is opened for reading.

Reading from a File:

Once a file is opened, you can read its contents using various methods. The most commonly used methods are read(), readline(), and readlines().
```
# Using read()
content = file.read()
print(content)

# Using readline()
line = file.readline()
print(line)

# Using readlines()
lines = file.readlines()
for line in lines:
    print(line)
```

### Writing to a File:

To write data to a file, you need to open it in write mode ("w"). If the file doesn't exist, it will be created. If it already exists, 
its previous contents will be overwritten.
```
file = open("output.txt", "w")
file.write("This is some text.")
file.close()
```
In the above example, the text "This is some text." is written to the file named output.txt. After writing, it's important to close the file using the close() method to release system resources.

Appending to a File:

To append data to an existing file without overwriting its contents, you can open the file in append mode ("a").
```
file = open("output.txt", "a")
file.write(" This is additional text.")
file.close()
```

In the above example, the text "This is additional text." is appended to the existing contents of the output.txt file.

Closing a File:

As mentioned earlier, it's important to close the file after you're done with it. This ensures that any changes made to the file are saved 
and system resources are freed.
```
file.close()
```
**Using the with Statement:**

Python provides a more convenient way to work with files using the with statement. It automatically takes care of opening and closing the file, 
even if an exception occurs.
```
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```
In the above example, the file is automatically closed when the with block is exited, eliminating the need for an explicit close() call.

These are the basic file handling operations in Python. You can perform more advanced tasks like reading CSV files, working with binary files, and handling exceptions while working with files. The Python os and shutil modules provide additional 
functionalities for file and directory operations.























