# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file
Save each script in a file with a .bat extension.
Ensure you have the necessary permissions to perform the operations.
Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "MyLab" on the desktop.


## COMMAND AND OUTPUT
```
mkdir %userprofile%\Desktop\MyLab
```
![435922084-46879a6b-01ab-4c9e-84f4-de16bda9746b](https://github.com/user-attachments/assets/3a54affb-0d55-4dfd-bedb-a31b672bca02)



Change to the "MyLab" directory and create an empty text file named "MyFile.txt" inside it.


## COMMAND AND OUTPUT
```
cd %userprofile%\Desktop\MyLab
```

![435922569-9f3f1ed4-b355-4b08-b471-ab6a6f81efb6](https://github.com/user-attachments/assets/41ef69e2-4d99-4afc-8d43-84e80c6416e2)

type nul > MyFile.txt

![435922810-7a1b0924-fab3-4488-a155-3b29007e4dc7](https://github.com/user-attachments/assets/1e110155-debb-49fd-983f-778872cbdd1c)



List the contents of the "MyLab" directory.


## COMMAND AND OUTPUT

Copy "MyFile.txt" to a new folder named "Backup" on the desktop.
```
dir %userprofile%\Desktop\MyLab
```

![435923101-e2a98080-3a42-4dde-b33e-a30c09f16e3b](https://github.com/user-attachments/assets/695d1a58-702f-4567-9afe-72cffd3a53c9)

copy MyFile.txt %userprofile%\Desktop\Backup

![435923497-b3b61c51-8a9c-4b66-b668-be67c998813d](https://github.com/user-attachments/assets/1a016358-b8ef-46f2-8e01-6928e7127f42)



## COMMAND AND OUTPUT

Move the "MyLab" directory to the "Documents" folder.
```
mkdir %userprofile%\Desktop\Documents
```

![435923682-ff8d7ba9-20c7-4d71-a6bf-ba820c40c22b](https://github.com/user-attachments/assets/b3382b0c-ab25-4369-8509-61ea2a32c238)



## Exercise 2: Advanced Batch Scripting

Create a batch script named "BackupScript.bat" that creates a backup of files with the ".docx" extension from the "Documents" folder to a new folder named "DocBackup" on the desktop.

```
@echo off
mkdir %userprofile%\Desktop\DocBackup
copy %userprofile%\Documents\*.docx %userprofile%\Desktop\DocBackup
echo Backup completed successfully!
```

## OUTPUT

![435924228-063d581e-0fbe-491a-8a98-f7246c5d044c](https://github.com/user-attachments/assets/44cdeb1d-1cfd-45e8-9e2a-2197e66bca8f)




# RESULT:
The commands/batch files are executed successfully.

