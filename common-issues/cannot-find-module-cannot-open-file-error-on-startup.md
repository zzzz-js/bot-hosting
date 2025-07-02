# Cannot find module / Cannot open file error on startup

Node.js\
\
`Cannot Find Module 'MODULENAME OR FILE DIRECTORY'`
---------------------------------------------------

1. You didn't declare the module in the package.json file or you don't have the file. For both cases, please follow [this explanation](https://discord.com/channels/884145104401608735/1348063335320653904/1348063391377395873).
2. Either your start file does not exist/is in the wrong directory and you need to change the start file name in the `Startup` tab or a file your code requires is missing (code issue, unrelated to the hosting).
3. A file you have requires another file in a specific directory. You either don't have that file or it is in a wrong directory. For both cases, this is an issue with your code and we cannot help you with that, you need to fix your bot code and make sure that it works locally before hosting it here.\
   \


## Python&#x20;

\
`ModuleNotFoundError: no module named 'MODULENAME'` or `/usr/local/bin/python: can't open file '/home/container/bot.py': [Errno 2] No such file or directory`

1. You didn't install the module of the error with the requirements.txt file or you don't have it. For both cases, please follow [this explanation](https://discord.com/channels/884145104401608735/1348063335320653904/1348063477402697880).
2. Either your start file does not exist/is in the wrong directory and you need to change the start file name in the `Startup` tab or a file your code requires is missing (code issue, unrelated to the hosting).
3. An error occurred before of this error, please check your console and if you cannot identify that error, open a support ticket.
