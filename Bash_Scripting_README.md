Bash Scripting

Here are smart answers to the provided questions:

1. **Write a program to count the number of times each word is present in a string and save it in a dictionary:**
   ```python
   def count_words(string):
       words = string.split()
       word_count = {}
       for word in words:
           word_count[word] = word_count.get(word, 0) + 1
       return word_count
   ```

2. **Script to change the password for one member out of three with the same password:**
   ```bash
   #!/bin/bash
   # Assuming passwords are stored in an array
   passwords=("password1" "password2" "password1")
   passwords[2]="new_password"
   ```

3. **Script to push a repository and build a job in Jenkins:**
   ```bash
   #!/bin/bash
   git push origin master
   curl -X POST http://jenkins-url/job/job-name/build
   ```

4. **Explanation of EC2 and VPC and script to create them:**
   EC2 (Elastic Compute Cloud) is a web service that provides resizable compute capacity in the cloud, and VPC (Virtual Private Cloud) is a virtual network dedicated to your AWS account. Below is a basic script to create an EC2 instance and VPC using AWS CLI:
   ```bash
   aws ec2 run-instances --image-id ami-123456 --instance-type t2.micro --key-name my-key --security-group-ids sg-123456
   aws ec2 create-vpc --cidr-block 10.0.0.0/16
   ```

5. **Experience using Bash shell scripts for version control and automating tasks:**
   In my previous role, I utilized Bash scripts to automate Git operations such as cloning repositories, pulling latest changes, and pushing commits. Additionally, I integrated Bash scripts into CI/CD pipelines to automate testing and deployment processes.

6. **Experience using Bash shell scripts for system administration tasks:**
   I have employed Bash scripts extensively for system administration tasks, including automating server configurations, managing users and permissions, and monitoring system resources. For example, I developed scripts to automate server provisioning, configure network settings, and monitor server performance.

7. **Experience using Bash scripts to manage files and directories:**
   Bash scripts have been instrumental in managing files and directories efficiently. For instance, I've created scripts to automate backups, synchronize files between servers, and clean up temporary files. By leveraging commands like `rsync`, `tar`, and `find`, I've been able to streamline file management tasks and ensure data integrity.

8. **Explanation of using bash scripts to manage processes and system resources:**
   Bash scripts have played a crucial role in managing processes and system resources effectively. For instance, I've developed scripts to monitor CPU and memory usage, automate the start and stop of services, and schedule tasks using cron jobs. By utilizing commands like `ps`, `top`, and `free`, I've gained insights into system performance and optimized resource allocation.

9. **Experience using bash scripts to automate repetitive tasks:**
   Bash scripts have been invaluable for automating repetitive tasks and improving productivity. For example, I've created scripts to automate software installations, configure environment variables, and perform routine maintenance tasks. By encapsulating sequences of commands into reusable scripts, I've minimized manual effort and ensured consistency across environments.

10. **Experience using bash scripts for system administration tasks:**
    Bash scripts have been a cornerstone of my system administration toolkit. I've leveraged them to automate user management, configure network settings, and troubleshoot system issues. For instance, I've developed scripts to provision new servers, configure firewall rules, and analyze log files. By combining Bash scripting with other tools and utilities, I've streamlined administrative tasks and enhanced system reliability.
