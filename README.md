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




## COMMAND AND OUTPUT
mkdir my-folder

![image](https://github.com/user-attachments/assets/dd5508d8-6d9b-491c-a5c0-b461cc6587a2)


Remove the directory "my-folder"

## COMMAND AND OUTPUT
rmdir my-folder

![image](https://github.com/user-attachments/assets/350a5a3b-99cf-4e6a-ab22-47107de8291b)



Create the file Rose.txt

## COMMAND AND OUTPUT
dir Rose.txt

![image](https://github.com/user-attachments/assets/a54ca95d-a707-4d6a-b58c-b24242b4cfbf)


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
echo “hello world” > hello.txt
type hello.txt

![image](https://github.com/user-attachments/assets/5b5384f3-a2fd-4d6c-96d0-0bc0c27188e0)


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
copy hello.txt hello1.txt

![image](https://github.com/user-attachments/assets/ecd36145-70b3-48dc-9bc2-48289bcb9fa5)


Remove the file hello1.txt

## COMMAND AND OUTPUT
del hello1.txt


![image](https://github.com/user-attachments/assets/c68f5a7e-14d9-41b8-a301-ed242a5c5616)


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
dir hello1.txt

![image](https://github.com/user-attachments/assets/f1f381d2-8b23-4815-b131-f0e593ea98ad)

List out all the associated file extensions 

## COMMAND AND OUTPUT
assoc | more

![image](https://github.com/user-attachments/assets/6be20cda-5f44-43c8-b14a-09a76bd6a59d)

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
fc hello.txt Rose.txt

![image](https://github.com/user-attachments/assets/eea324f4-1e91-45d3-84a9-cd711c97069f)

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/f3404292-c190-429a-bc6d-ff29bf00823c)


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/260d2633-fc3c-460e-9fd8-07c8c9ad3746)


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```

## OUTPUT

![image](https://github.com/user-attachments/assets/2e386ffd-877b-4aee-9b0a-2bf6d6e916c7)



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause

```

## OUTPUT



Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause

```
## OUTPUT

![image](https://github.com/user-attachments/assets/9e4e4f0b-e1f1-4bea-bf47-3b6a3a67915f)


# RESULT:
The commands/batch files are executed successfully.

