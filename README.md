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

Remove the directory "my-folder"





## COMMAND AND OUTPUT


Create the file Rose.txt



<img width="604" height="109" alt="image" src="https://github.com/user-attachments/assets/d9fed525-96a3-4826-98f9-668f3a8dbbe3" />

## COMMAND AND OUTPUT


Create the file hello.txt using echo and redirection



<img width="660" height="137" alt="image" src="https://github.com/user-attachments/assets/0d348bd0-2e3e-4abb-9b00-8ae4b7daae37" />

## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt


<img width="635" height="117" alt="image" src="https://github.com/user-attachments/assets/39ec7767-558a-483f-84a1-2aa3303916a2" />


## COMMAND AND OUTPUT

Remove the file hello1.txt



## COMMAND AND OUTPUT

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

List out all the associated file extensions 

## COMMAND AND OUTPUT


Compare the file hello.txt and rose.txt

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


<img width="1235" height="173" alt="image" src="https://github.com/user-attachments/assets/0fa4bfbf-3f48-4eda-ae98-f49f9a728f4b" />




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
<img width="1232" height="528" alt="image" src="https://github.com/user-attachments/assets/a93f7325-907e-4530-a65b-2618e676f754" />





Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause
```





## OUTPUT



<img width="1236" height="396" alt="image" src="https://github.com/user-attachments/assets/b88953c8-2821-4a08-8434-8c10159a86bb" />






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


<img width="1169" height="135" alt="image" src="https://github.com/user-attachments/assets/a3b2f61e-3199-4110-8f2f-aa9d40c78c18" />



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

<img width="1342" height="522" alt="image" src="https://github.com/user-attachments/assets/28d57918-a10d-49fd-880c-6fda21c5fa78" />




# RESULT:
The commands/batch files are executed successfully.

