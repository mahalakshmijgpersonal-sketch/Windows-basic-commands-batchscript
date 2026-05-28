# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
## COMMAND AND OUTPUT
Create the directory "my-folder"



<img width="606" height="223" alt="image" src="https://github.com/user-attachments/assets/f1d119b2-d755-4f8c-bc9a-f0e58b35cbb9" />




## COMMAND AND OUTPUT

Remove the directory "my-folder"



<img width="842" height="371" alt="image" src="https://github.com/user-attachments/assets/2f0890f0-21e2-4857-9c04-8de68f661d0a" />






## COMMAND AND OUTPUT


Create the file Rose.txt


<img width="828" height="352" alt="image" src="https://github.com/user-attachments/assets/53500d5e-b732-47d7-8bfe-79be69aa94ce" />




## COMMAND AND OUTPUT


Create the file hello.txt using echo and redirection



<img width="960" height="121" alt="image" src="https://github.com/user-attachments/assets/5649147d-cc1d-4be4-9bcf-a81ad0d50069" />




## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt



<img width="892" height="143" alt="image" src="https://github.com/user-attachments/assets/abcdd0a6-4b7f-40bf-8f8e-09ef5ae5b195" />



## COMMAND AND OUTPUT

Remove the file hello1.txt



<img width="782" height="221" alt="image" src="https://github.com/user-attachments/assets/f853f4d2-7049-4bbb-9b52-b0a7dce14613" />



## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory



<img width="757" height="1059" alt="image" src="https://github.com/user-attachments/assets/a4efc4ab-40aa-4ede-9daa-3e4e814d0f20" />



## COMMAND AND OUTPUT

List out all the associated file extensions 


<img width="863" height="1106" alt="image" src="https://github.com/user-attachments/assets/2992ebb5-ffb2-4b38-9a12-0c2cf0539c90" />





## COMMAND AND OUTPUT


Compare the file hello.txt and rose.txt



<img width="826" height="188" alt="image" src="https://github.com/user-attachments/assets/9abda4f7-7a85-4f74-a527-781d9fcbb728" />




## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%
pause
```





## OUTPUT



<img width="697" height="89" alt="image" src="https://github.com/user-attachments/assets/4d44098f-f71a-4d20-871c-39696b642ae7" />





Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off

:START

set /p num=Enter a number: 

set /a rem=%num% %% 2

if %rem%==0 (
    echo The number is Even
) else (
    echo The number is Odd
)

set /p choice=Do you want to continue (Y/N)? 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid Input
goto START

:END
echo Thank You
pause

```






## OUTPUT


<img width="693" height="260" alt="image" src="https://github.com/user-attachments/assets/f73f084f-0b7d-4b93-bd1a-085be10b8242" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause
```





## OUTPUT



<img width="715" height="209" alt="image" src="https://github.com/user-attachments/assets/c94cd1e6-aac0-4941-ad79-3e5806784dcf" />







Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off

if exist sample.txt (
    echo sample.txt exists
) else (
    echo sample.txt does not exist
)

pause
```

## OUTPUT



<img width="696" height="111" alt="image" src="https://github.com/user-attachments/assets/91acea36-5a0d-477b-9898-a0529306e305" />




Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off

:MENU
echo ====================
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
echo ====================

set /p choice=Enter your choice: 

if %choice%==1 goto HELLO
if %choice%==2 goto CREATE
if %choice%==3 goto EXIT

echo Invalid Choice
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File Created
pause
goto MENU

:EXIT
echo Goodbye
pause
exit
```


## OUTPUT




<img width="753" height="442" alt="image" src="https://github.com/user-attachments/assets/6649c596-c50d-4933-8f10-e0e71e8ea66d" />



# RESULT:
The commands/batch files are executed successfully.

