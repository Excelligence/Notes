## How to Find out what is working on a certain port on you computer and kill it

to find what is working on port 5500 on windows use this command

`netstat -ano | findstr :5500`

Now you have to kill the task which is running on that port

`taskkill /PID <typeyourPIDhere> /F`



