# Host-check
Remote multi-server tool to check server status. The tool opens a windows notification to display the results.

#Screenshots
###### Problems found
![Problems found](/screenshots/error_found.png)

###### No problems found
![No problems found](/screenshots/no_error.png)

#Environments 
The tool can be used only in Windows.

#Requirements
The tool requires Python 3.4. You should also install the 'win32gui'.

#Running the tool
###### Execute
```python host_check.pyw```

###### Single use
Set *mode = "single"* in the config.conf (default). The Windows notification will display a *All servers are up* message if all servers respond. Alternatively, the Winodws notification will display the servers that did not respond. 

###### Scheduler
Set *mode = "scheduler"* in the config.conf. You can create a Windows task to run the tool automatically. *scheduler* mode will only display a Windows notification if any servers do not respond. If all servers respond no Windows notification will be displayed.

#Configuration
Add nodes in the *config.conf* file:
```
servers = [["server_1_name",port],
["server_2_name",port]
```

#Credits
I use the balloon tip code found here:
[ wontoncc/balloontip.py](https://gist.github.com/wontoncc/1808234)










