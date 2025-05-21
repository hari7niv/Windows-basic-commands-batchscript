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

## 1. Create a directory named "my-folder"

## COMMAND AND OUTPUT
```
mkdir my-folder
```
![Screenshot 2025-05-19 080712](https://github.com/user-attachments/assets/edd645dc-9868-4d16-9834-0eff7fb6e85d)


## 2. Remove the directory "my-folder"
## COMMAND AND OUTPUT
```rmdir my-folder```

![Screenshot 2025-05-19 080735](https://github.com/user-attachments/assets/9d228676-8da1-4934-9575-dcbd215529c4)


## 3. Create the file Rose.txt
## COMMAND AND OUTPUT
```COPY CON Rose.txt```

![Screenshot 2025-05-19 093309](https://github.com/user-attachments/assets/c1ef4bc7-8b32-4db6-9449-2d659cf1de67)



## 4. Create the file hello.txt using echo and redirection
## COMMAND AND OUTPUT
```
echo “hello world” > hello.txt
type hello.txt
```

![Screenshot 2025-05-19 093408](https://github.com/user-attachments/assets/e22968a0-8ea5-40ce-a3fa-089c277c4444)


## 5. Copy the file hello.txt into the file hello1.txt
## COMMAND AND OUTPUT
```
copy hello.txt hello1.txt
```

![Screenshot 2025-05-19 093450](https://github.com/user-attachments/assets/3f8fa4f7-cf0b-443b-b475-f0b23e7d504d)


## 6. Remove the file hello1.txt
## 7. List out the file hello1.txt in the current directory
## COMMAND AND OUTPUT
```
del hello1.txt
dir hello1.txt
```

![Screenshot 2025-05-19 093516](https://github.com/user-attachments/assets/80676924-ea0e-43a3-a66b-de4899fb4a96)

## 8. List out all the associated file extensions 
## COMMAND AND OUTPUT
```assoc | more```

![Screenshot 2025-05-19 093548](https://github.com/user-attachments/assets/61a6ab44-7c83-4294-8f63-9c6135e19255)



## 9. Compare the file hello.txt and rose.txt
## COMMAND AND OUTPUT
```fc hello.txt Rose.txt```

![Screenshot 2025-05-19 093722](https://github.com/user-attachments/assets/84aeafa9-ef05-4444-a043-d83dccafdb3b)


## Exercise 2: Advanced Batch Scripting
## 1. Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT
![Screenshot 2025-05-19 093948](https://github.com/user-attachments/assets/06b50bc3-dccc-48b9-aada-a2b221e40b3e)




## 2. Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
### 1. Prompt the user to enter a number.
### 2. Calculate the remainder when the number is divided by 2.
### 3. Display whether the number is odd or not.
### 4. Ask the user if they want to check another number.
### 5. Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
### 6. Handle invalid inputs for the continuation prompt (Y/N) gracefully.

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
![Screenshot 2025-05-19 094225](https://github.com/user-attachments/assets/35face2b-67de-4d56-9872-dfdf2806bca2)




## 3. Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT
![Screenshot 2025-05-19 094256](https://github.com/user-attachments/assets/b58ba818-262a-4c3b-b9a7-c4e4316b4578)




## 4. Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

### Instructions:
### 1. Use the IF EXIST conditional statement.
### 2. Make sure the script works for files located in the same directory as the batch file.
### 3. Use pause to keep the command window open after displaying the message.
### 4. Expected Output (if the file exists):

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
![Screenshot 2025-05-19 094357](https://github.com/user-attachments/assets/08551de9-966f-4de3-92af-07f1b7625484)



## 5. Write a batch script that displays a simple menu with three options:
### 1. Say Hello – Displays the message Hello, World!
### 2. Create a File – Creates a file named newfile.txt with the content This is a new file
### 3. Exit – Exits the script with a goodbye message
### 4. The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

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
![Screenshot 2025-05-19 094556](https://github.com/user-attachments/assets/b0b436cd-e9bd-415a-8309-880a98ccce05)



# RESULT:
The commands/batch files are executed successfully.


### Name : ASWIN B
### Register Number : 212224110007

