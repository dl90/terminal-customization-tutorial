---
layout: default
title: File CRUD Operations
nav_order: 4
has_children: false
permalink: /docs/files
---

{: .fs-6 .fw-300 }

# File CRUD Operations
{: .no_toc }

---

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## What is CRUD

If you are in the technical field, often times you will need to create new files to work with. By being familiar with how to create and manipulate files in the terminal, you may save yourself a bit of hassle and time. 

_CRUD_ is an acronym that stands for create, read, update, and delete. These are the most basic actions that you can perform on files.

---

## CRUD Instructions

This instruction set will go over Linux commands that allow you to perform _CRUD_ actions in the terminal. You will use the `touch` command to create new files, the `cat` command to read and update files, and the `rm` command to delete unwanted files.

 You will also learn how to copy and move files using the `mv` command.

---

**1.** Input the following command into your terminal to create a new file.

>```
>touch test.txt
>```

>Test if the *`test.txt`* file is inside the directory with the following command.

>```
>ls
>```

>You can see that the file named *`test.txt`* exists inside your current directory.

>![Root user](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/rootuser.png?raw=true "Root user")
<br />
<br />

**2.** Enter the following command to read the contents of the file.

>```
>cat test.txt
>```

>You will notice that there is no output. That's because nothing was input into the *`test.txt`* file!
<br />
<br />

**3.** Insert some text into the new file with the following command.
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: Ensure that you add *`>`* to the command this time to be able to insert text into the file.
<br />
<br />

>```
>cat > test.txt
>```

>Enter some text of your choice into the empty field and hit **[return]**. I will enter the following text into my file.

>```
>I am a test line.
>```
<br />

**4.** Enter the `cat` command once again to check the contents.

>```
>cat test.txt
>```

>You will see that we did indeed change the contents of the *`test.txt`* file.

>![Inserted text into test.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/insert-text.png?raw=true "test.txt has contents")
<br />
<br />

**5.** Input the following command to rename our *`test.txt`* file into *`newname.txt`*.
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: When using the `mv` command to rename a file, enter the current file name and then the new name.
<br />
<br />

>```
>mv test.txt newname.txt
>```

>Check your current directory again to see that the file name change.

>```
>ls
>```

>You will notice that *`newname.txt`* exists instead of *`test.txt`*.

>![Renamed .txt file](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/renamed.png?raw=true "Renamed .txt file.")
<br />
<br />

**6.** Move your *`newname.txt`* file to a different directory with the following commands.
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: You may notice here that you use the `mv` command to move a file into a different directory by entering the file name and then the directory name.
<br />
<br />

>Create a new directory to move the *`newname.txt`* file inside.

>```
>mkdir myfolder
>```

> Move *`newname.txt`* inside the new directory *`myfolder`*.

>```
>mv newname.txt myfolder
>```

>Check the contents of the directory *`myfolder`*.

>```
>ls myfolder
>```

>You should notice that *`newname.txt`* did indeed move inside of the *`myfolder`* directory.

>![Moved .txt file](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/moved.png?raw=true "Moved .txt file.")
<br />
<br />

**7.** Remove the *`newname.txt`* file and the *`myfolder`* directory using the `rm` command.
<br />

>![Caution icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/caution.png?raw=true "Caution"){: style="float: left" } 
>> **Caution**: You need to first delete the contents before being able to delete the directory.
<br />
<br />

>Remove *`newname.txt`* from the *`myfolder`* directory by stating the directory and the file you want to remove with the following command.

>```
>rm myfolder/newname.txt
>```

>Remove the *`myfolder`* directory completely with the following command.

>```
>rmdir myfolder
>```
<br />

You will see that you have completely removed both the directory and the contents using the `ls` command. You should no longer see both the .txt file and directory.

As you've noticed by now, you were able to do these things without the use of your mouse or a graphical user interface. You should be able to use these commands for your own future use in Linux when the need to create new file types and directories arise.

The next step is to learn how to [find processes and how to stop them.](https://dl90.github.io/linux-basics/docs/processes)
