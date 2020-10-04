The concept behind this second project was to familiarize ourselves with what bash, shell, and scripting is within git bash. The first step was to simply type the commands: "date", "cal", "pwd", and "ls". All of these commands worked properly except for "cal" which give me an error stating "bash: cal: command not found". The next step was to practice scripting by creating a new file in vi but our instructions stated that we needed to use nano instead. When I used nano, I noticed it was more user friendy than vi was and listed helpful commands towards the bottom. I typed the same commands in the first part inside of nano and then saved my file within my "Documents" folder. After this, I used chmod +x to make my file executable and then ran it with "./". I noted that the only program that did not run was the "cal" command so I did not see a calendar on my screen. I used nano to go back into the newly created task.sh file and added "#!/bin/bash" which allows the script's interperter to be defined as Bash. The next section in this tutorial we had to use the command file to see the identify of the "hello world" file. It was a shell script, ASCII text executable file. I used the copy command after to send the standard output of the file "hello world" to a new named "0_vyz". A quick check of the command "file" proves that contents were successfully copied from file "hello world". I used nano to go insde the file and delete the line at the header "#!/bin/bash". After saving and quitting, I used file to see the new identity and it was changed to just ASCII text. The next step in the tutorial was to see an alternate way to use execute a script and that was used by simply saying "bash filename". This way is a lot cleaner and there is no need to use a text editor. The last part in the tutorial was learning the difference between an absolute path and a relative path. Knowing the difference between the two is crucial when changing directories and when sending content to other files. Simply put, if you are within the directory of the file which you are executing a command for then you are in a relative path and do no have to explicitly state the path with "/etc..". However, if you are in a seperate directory, you have to state the path explicitly with multiple "/" so that whatever action you peform can be properly executed. A really good command that can be used here is "pwd" or print working directory which tells you which directory you are currently in.

After playing along with the tutorial on linuxconfig.org as mentioned in the above paragraph, I started with my first script that I named "hello-world.sh". The first step was to create the file, the instructions don't say to use "touch" which is what I am used to using to create a new file. Instead, the instructions say to use "vi". As a side note, I did not use "nano" as stated in the PDF instructions because I have never used it and was confusing myself because I am already used to using "vi" and "vim". So from now on, every action in a text editor I used was with "vi" and not "nano". I created the new file using vi and then wrote the shebang along with echo "Hello World". Echo is a command used to display a string of text. After writing this in the newly created "hello-world.sh" file I hit the ESC button and used "wq" to save and quit my work in vi. I used "chmod +x" to change the access file permissions and subsequently wrote "./" and then the file nam to execute the newly created script. The end output was "Hello World" and everything ran correctly. 

The next script I created was "backup.sh". I had difficulty with this script creation. The very beginning you have to use command "tar -czf" to create a compressed tall bar of the entire user home directory. I understood the process of what was happening but for my tar command to work I needed to change the directory from what the example had to what my home directory was. However, I had difficulty making this work and what ended up working for me was using the path "/c/morej/Documents". After I specified this path, I was able to use the "tar" command and then use the "rm" command to remove the "tmp" directory. The instructions then called for a use of the "which" command with bash to print a full path to the newly created "backup.sh" file. To finialize this script, I used "echo" followed by the tar command and then appended it to the backup.sh file with ">>". Then I used vi to check if the content had been added to the backup.sh file and it did. I adjusted the shebang within the backup.sh file to include the "#" and then used the same "chmod +x" and "./" commands to make the file executable. The end output I received was the following line "tar: Removing leading /' from member names". I wasn't sure if that was the correct output or not but based on the videos, I want to say that it was, and it was working correctly. 

The next script that I created was "welcome.sh" this was simple enough. All I did was create a the new file using vi and within the text file add commands that would print out the user and what version of the bash shell there were running. This was done using two echos and having three variables named greeting, user, and day. The end output after executing was the following: "Welcome back morej! Today is Saturday, which is the best day of the entire week! Your Bash shell version is "4.4.23(1)-release. Enjoy!". This script was running correctly.

In between writing the next script, I praticted using variables by assigning values and then using echo with simple arithmetic to print out those values in one line. Practicing this led to a change I had to make in the "backup.sh" file. I rewrote was in that file and replaced it with parameters which are noted with the curly brackets. After replacing the text within this file, I received an error with executing that stated "tar: /home/morej: Cannot Stat: No such file or directory". I was not able to fix this problem after searching online and the instructions were not help because in the example they are using their own personal home directory. The updated "backup.sh" was not working as intended and was incorrect. 

