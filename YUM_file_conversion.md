
## Software Management Lab - Working with Transaction History (yum)
`Login user` — the name of the user whose login session was used to initiate a transaction. This information is typically presented in the `Full Name <username>` form. 
Below begins a demonstration of the file conversion process using a text editor to change view outputs for the “yum history” command. (The text editor is a factor of choice based on your personal use and experience). For this example `nano` will be utilized. The yum configuration  file is stored with most other configuration and system files within the `/etc` directory. By default `etc` isn’t quotable Therefore, make sure to use “sudo” command. 

The below output shows `httpd -y` instead of `EC2… <ec2-user>`

```
[ec2-user@ip-10-0-10-232 companyA]$ sudo yum history list
Loaded plugins: extras_suggestions, langpacks, priorities, update-motd
ID     | Command line             | Date and time    | Action(s)      | Altered
-------------------------------------------------------------------------------
     1 | install httpd -y         | 2023-02-21 22:13 | Install        |    9
history list
```

The following Screenshot below show the nano file editor GUI with the “yum.conf” file opened


Track your cursor to the first available line input the following: history_list_view=users 
Save file changes with key sequence (^O=Ctrl+O Write Out) Press ENTER to confirm..


Close Nano file editor with key sequence (^X=Exit) 

Rerun sudo yum history list command and observe the output

```
[ec2-user@ip-10-0-10-175 companyA]$ sudo yum history list
Loaded plugins: extras_suggestions, langpacks, priorities, update-motd
ID     | Login user               | Date and time    | Action(s)      | Altered
-------------------------------------------------------------------------------
     1 | EC2 ... <ec2-user>       | 2023-02-21 00:15 | Install        |    9
history list
[ec2-user@ip-10-0-10-175 companyA]$
```

