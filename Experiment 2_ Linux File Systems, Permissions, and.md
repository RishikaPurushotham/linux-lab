
**Experiment 2: Linux File Systems, Permissions, and Essential Commands**

* * *
Name: Rishika Purushotham Roll No.: 590029145 Date: 2025-09-23
* * *
**Aim**:
- To understand the structure of Linux file systems.
- To learn and practice essential navigation and file management commands.
- To explore file permissions and ownership, and manage them using Linux commands.
- To use user management, system information commands, and editing tools.
- To solve practical exercises and tasks for mastering Linux basics.
  
* * *
**Requirements**

- A Linux machine (Ubuntu/Debian/Linux Mint or similar).
-User privileges to create, modify, and delete files.
-Access to terminal and text editors like nano or vim .
* * *
**Theory**

Linux uses a hierarchical file system starting from the root / . Essential directories include /home , /etc , /usr , /var , /bin , and /tmp . 
File permissions are divided among owner, group, and others,
with actions r (read), w (write), and x (execute). Navigation commands like ls , pwd , cd , and file operations ( cp , mv , rm ) form the basis of Linux usage. Editors ( nano , vim ) and commands for system info ( uname , df , top , history ) provide insights and control. Practice tasks build practical
confidence.
* * *
**Procedure & Observations**

**Section 1: File Systems and Permissions**
We learned how Linux organizes directories, how to view and change file permissions using chmod ,
chown , and chgrp .

**Section 2: Navigation and File Operations**
Commands like ls , pwd , cd , mkdir , rmdir , touch , cp , mv , rm were practiced to manage files and
directories.

**Section 3: File Viewing and Editing**
We used cat , less , head , tail to view file contents, and practiced editing with nano and vim .

**Section 4: User Management**
Commands whoami , who , passwd , sudo were practiced to understand users and privileges.

**Section 5: System Information**
Commands like uname , df , top , htop , history were used to gather system and process information.

**Section 6: Practice Exercises**
Hands-on practice included navigation, file operations, text editing, system exploration, and cleanup.

* * *

**Practice Exercises**
 Exercise 1: File System Navigation
cd
pwd
mkdir -p projects/linux_practice/{scripts,documents,backup}
cd projects/linux_practice/scripts
touch setup.sh cleanup.sh readme.txt
ls -la
cd ..
ls -la

Output:
![216a260b964abc6970e17badea7799e3.png](../_resources/216a260b964abc6970e17badea7799e3.png)

Exercise 2: File Operations and Permissions

cd ~/projects/linux_practice/documents
echo "This is a practice document" > practice.txt
ls -l practice.txt
chmod 644 practice.txt
cp practice.txt ../backup/
cp practice.txt ../backup/practice_backup_$(date +%Y%m%d).txt
ls -la ../backup/

Output:
![04a70ef678162b2f3e2870f715cce4f2.png](../_resources/04a70ef678162b2f3e2870f715cce4f2.png)


Exercise 3: Text Editing and Viewing
cd ~/projects/linux_practice/documents
seq 1 50 > numbers.txt
head numbers.txt
tail -n 5 numbers.txt
cat numbers.txt | grep "25"
nano numbers.txt
cat numbers.txt

Output:
![9736949b6e6cc86ae418df06179200b5.png](../_resources/9736949b6e6cc86ae418df06179200b5.png)
![67737d721d361f9a033796cc7f6f397b.png](../_resources/67737d721d361f9a033796cc7f6f397b.png)
![8f1aa68cd75beb4745026091301e8936.png](../_resources/8f1aa68cd75beb4745026091301e8936.png)
![bd48494afd5fabc7fdb130774bf95fda.png](../_resources/bd48494afd5fabc7fdb130774bf95fda.png)


Exercise 4: System Exploration
uname -a
df -h
history 10
who
whoami
top

Output:
![19d6c10ce3abf7af4f45040155bc6f6b.png](../_resources/19d6c10ce3abf7af4f45040155bc6f6b.png)
![7e105e79e7b52efa699de85084b20f4a.png](../_resources/7e105e79e7b52efa699de85084b20f4a.png)

Exercise 5: Cleanup
cd ~/projects/linux_practice
rm -i documents/numbers.txt
rmdir backup
rm -r backup
ls -la
history | tail -20

Output:
![0f1ce112a467259ea00f0a6e5fc7a0b3.png](../_resources/0f1ce112a467259ea00f0a6e5fc7a0b3.png)

**Question Bank / Lab Exam Tasks**

- Task 1: Directory Navigation
mkdir -p ~/test_project/{docs,scripts,data}
cd ~/test_project/scripts
pwd

Output:
![06665514fb546f8cea3e1c29cd3bae31.png](../_resources/06665514fb546f8cea3e1c29cd3bae31.png)

- Task 2: File Creation and Content
cd ~/test_project/docs
touch readme.txt notes.txt todo.txt
echo "Project documentation" > readme.txt
echo "Important notes" > notes.txt
cat readme.txt
cat notes.txt

Output:
![c0c1f22d82d5ffdcd9594bcb0bdc4a68.png](../_resources/c0c1f22d82d5ffdcd9594bcb0bdc4a68.png)

- Task 3: File Operations
cp readme.txt ../data/project_info.txt
mv todo.txt ../scripts/

Output:
![1cefa4a665deac84b04d87850044ebde.png](../_resources/1cefa4a665deac84b04d87850044ebde.png)

- Task 4: File Permissions
cd ~/test_project/scripts
echo "#\!/bin/bash" > backup.sh
echo "echo Backup complete" >> backup.sh
chmod u+x backup.sh
ls -l backup.sh

Output:
![0003c64a80ccb3e8bb8daf5692a76d31.png](../_resources/0003c64a80ccb3e8bb8daf5692a76d31.png)


- Task 5: File Viewing
seq 1 20 > numbers.txt
head -n 5 numbers.txt
tail -n 3 numbers.txt
grep "1" numbers.txt

Output:
![9f688993c025b7c23700ff7db8d58f36.png](../_resources/9f688993c025b7c23700ff7db8d58f36.png)

- Task 6: Text Editing
nano config.txt
cat config.txt

Output:
![f98d7e2fc90cd8480aabf4ba462364d2.png](../_resources/f98d7e2fc90cd8480aabf4ba462364d2.png)

- Task 7: System Information
echo "Username: $(whoami)" > system_info.txt
echo "Date: $(date)" >> system_info.txt
echo "Directory: $(pwd)" >> system_info.txt
df -h >> system_info.txt
cat system_info.txt

Output:
![3e242bd7b67149da3a94dbd2e0047411.png](../_resources/3e242bd7b67149da3a94dbd2e0047411.png)

- Task 8: File Organization
mkdir ~/test_project/backup
cp ~/test_project/*/*.txt ~/test_project/backup/
ls -la ~/test_project/backup

Output:
![d35cc151a717d561b64ab1aaa2579d6f.png](../_resources/d35cc151a717d561b64ab1aaa2579d6f.png)

- Task 9: Process and History
history | wc -l
history 10

Output:
![611355aefc5f3af4e04b8bb43358be60.png](../_resources/611355aefc5f3af4e04b8bb43358be60.png)

- Task 10: Comprehensive Cleanup
chmod 754 backup.sh
find ~/test_project -type f | wc -l > summary.txt
find ~/test_project -type d | wc -l >> summary.txt
cat summary.txt

Output:
![dc86ee10494edc5b3312ec2800094d8e.png](../_resources/dc86ee10494edc5b3312ec2800094d8e.png)

**Result**
Explored Linux file system structure.
Practiced file operations, editing, and permissions.
Learned user and system management commands.
Completed practical exercises and lab exam-style tasks.
Challenges Faced & Learning Outcomes
- Challenge 1: Managing complex directory structures.
- Challenge 2: Remembering symbolic vs numeric permissions.
- Challenge 3: Using find , grep , and redirection effectively.

**Learning:**
Mastered Linux navigation, file handling, and permissions.
Gained practical knowledge of user/system management.
Practiced exam-style tasks to solidify learning.

**Conclusion**
This experiment comprehensively covered Linux file systems, permissions, commands, editing,
user management, and system info. The tasks ensured thorough practice, making it a complete
foundation for Linux proficiency.