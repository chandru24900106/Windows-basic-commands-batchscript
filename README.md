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
Create a directory named "my-folder"

## COMMAND AND OUTPUT
```
mkdir my-folder
```
<img width="525" height="91" alt="image" src="https://github.com/user-attachments/assets/ee5cb020-fc7d-4f8d-bae4-d2035ff89e5c" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT
```
rmdir my-folder
```
<img width="505" height="93" alt="image" src="https://github.com/user-attachments/assets/7c833e24-2c45-4ab3-b455-084d30422a76" />


Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="712" height="405" alt="image" src="https://github.com/user-attachments/assets/6888ea22-3146-40cc-ad20-d6fcf566ee76" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

<img width="682" height="112" alt="image" src="https://github.com/user-attachments/assets/fbd617a6-4326-4340-8b71-1f1b32fe5ce2" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

<img width="678" height="152" alt="image" src="https://github.com/user-attachments/assets/96b63462-a5fb-4fa3-8527-3bdd5237de25" />

Remove the file hello1.txt

## COMMAND AND OUTPUT

<img width="522" height="231" alt="image" src="https://github.com/user-attachments/assets/0d3a95b9-3653-4a7f-8ac4-0aa192b30868" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

<img width="523" height="645" alt="image" src="https://github.com/user-attachments/assets/0cecec97-cd96-43db-92ba-5ce8e7872125" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="587" height="917" alt="image" src="https://github.com/user-attachments/assets/b38d33bb-d4fa-42eb-87a3-402345396f01" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="593" height="212" alt="image" src="https://github.com/user-attachments/assets/d162b24c-d603-4c65-8dc3-352570af1f86" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause

```




## OUTPUT


<img width="428" height="111" alt="image" src="https://github.com/user-attachments/assets/2b5662f6-2ac5-4849-b7ce-f3f1f09f1b78" />


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


<img width="652" height="235" alt="image" src="https://github.com/user-attachments/assets/191cc84f-e4d4-4d2e-a2d1-149b990cf961" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```



## OUTPUT


<img width="457" height="191" alt="image" src="https://github.com/user-attachments/assets/08642cbb-4d16-4070-8b01-ba9559155e2a" />



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


<img width="663" height="222" alt="image" src="https://github.com/user-attachments/assets/9da29b04-ca3d-48e1-ace7-34c5796051b4" />


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

<img width="452" height="420" alt="image" src="https://github.com/user-attachments/assets/1bccaa57-0425-4386-a00c-0082da99cc72" />


# RESULT:
The commands/batch files are executed successfully.

