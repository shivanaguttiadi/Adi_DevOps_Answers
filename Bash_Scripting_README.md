Bash Scripting

Here are smart answers to the provided questions:

1. **Experience using Bash shell scripts for version control and automating tasks:**
   In my previous role, I utilized Bash scripts to automate Git operations such as cloning repositories, pulling latest changes, and pushing commits. Additionally, I integrated Bash scripts into CI/CD pipelines to automate testing and deployment processes.

2. **Experience using Bash shell scripts for system administration tasks:**
   I have employed Bash scripts extensively for system administration tasks, including automating server configurations, managing users and permissions, and monitoring system resources. For example, I developed scripts to automate server provisioning, configure network settings, and monitor server performance.

3. **Experience using Bash scripts to manage files and directories:**
   Bash scripts have been instrumental in managing files and directories efficiently. For instance, I've created scripts to automate backups, synchronize files between servers, and clean up temporary files. By leveraging commands like `rsync`, `tar`, and `find`, I've been able to streamline file management tasks and ensure data integrity.

4. **Explanation of using bash scripts to manage processes and system resources:**
   Bash scripts have played a crucial role in managing processes and system resources effectively. For instance, I've developed scripts to monitor CPU and memory usage, automate the start and stop of services, and schedule tasks using cron jobs. By utilizing commands like `ps`, `top`, and `free`, I've gained insights into system performance and optimized resource allocation.

5. **Experience using bash scripts to automate repetitive tasks:**
   Bash scripts have been invaluable for automating repetitive tasks and improving productivity. For example, I've created scripts to automate software installations, configure environment variables, and perform routine maintenance tasks. By encapsulating sequences of commands into reusable scripts, I've minimized manual effort and ensured consistency across environments.

6. **Experience using bash scripts for system administration tasks:**
    Bash scripts have been a cornerstone of my system administration toolkit. I've leveraged them to automate user management, configure network settings, and troubleshoot system issues. For instance, I've developed scripts to provision new servers, configure firewall rules, and analyze log files. By combining Bash scripting with other tools and utilities, I've streamlined administrative tasks and enhanced system reliability.

7. **Using bash scripts to interact with APIs or web services:**
   Bash scripts have facilitated interaction with APIs and web services through utilities like cURL. I've employed techniques such as parsing JSON or XML responses using tools like `jq` or `xmlstarlet` to extract relevant data and manipulate it as needed.

8. **Experience with bash scripts for debugging and troubleshooting:**
    Bash scripts have been instrumental in debugging and troubleshooting by incorporating error handling and logging mechanisms. Techniques such as echoing debug messages, using `set -x` for tracing, and redirecting error output have helped diagnose and resolve issues efficiently.

9. **Using bash scripts for implementing security controls:**
    Bash scripts have enabled the implementation of security controls by managing user permissions, enforcing firewall rules, and auditing system configurations. I've utilized commands like `chmod` and `chown` to manage file permissions and `iptables` to configure firewall rules, ensuring a secure environment.

10. **Experience with bash scripts for automating software installations and updates:**
    Bash scripts have automated software installations and updates by leveraging package managers like `apt` or `yum` and downloading packages from repositories. Techniques such as checking for dependencies, handling prompts, and configuring application settings programmatically have streamlined the process.

11. **Using bash scripts to integrate with other tools or services:**
    Bash scripts have facilitated integration with various tools and services, enabling automation of workflows and tasks. For instance, scripts have interacted with version control systems like Git to automate code deployments or integrated with CI platforms like Jenkins to trigger build jobs based on events or conditions.

**Scripting Level**


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
Sure, let's provide script-level answers for each scenario:

1. **Creating a backup script for a Linux server**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Define directories and backup destination
     SOURCE_DIR="/path/to/source"
     DEST_DIR="/path/to/backup"
     
     # Create backup filename with timestamp
     BACKUP_FILE="backup_$(date +"%Y%m%d_%H%M%S").tar.gz"
     
     # Create tar archive of directories
     tar -czf "${DEST_DIR}/${BACKUP_FILE}" "${SOURCE_DIR}"
     ```

2. **Monitoring disk usage on a macOS system**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Define disk usage threshold
     THRESHOLD="80"  # Adjust as needed
     
     # Get disk usage information and extract relevant data
     USAGE=$(df -H / | awk 'NR==2 {print $5}' | sed 's/%//')
     
     # Check if usage exceeds threshold and send alert
     if [ "${USAGE}" -gt "${THRESHOLD}" ]; then
         osascript -e 'display notification "Disk usage exceeds threshold!" with title "Disk Usage Alert"'
     fi
     ```

3. **Automating user provisioning on a Windows server**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Define PowerShell script for user provisioning
     PS_SCRIPT='
     param (
         [string]$username,
         [string]$password
     )
     
     New-LocalUser -Name $username -Password (ConvertTo-SecureString $password -AsPlainText -Force)
     '
     
     # Execute PowerShell script remotely on Windows server
     ssh user@windows-server "powershell -Command '${PS_SCRIPT}' -username 'newuser' -password 'password'"
     ```

4. **Parsing log files on a Unix-based server**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Search log files for error messages
     grep "ERROR" /var/log/application.log
     
     # Extract IP addresses from access log
     awk '{print $1}' /var/log/access.log
     ```

5. **Automating database backups on a Linux server**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Define database credentials
     DB_USER="username"
     DB_PASS="password"
     DB_NAME="database"
     
     # Define backup filename with timestamp
     BACKUP_FILE="backup_$(date +"%Y%m%d_%H%M%S").sql.gz"
     
     # Dump database contents to backup file
     mysqldump -u "${DB_USER}" -p"${DB_PASS}" "${DB_NAME}" | gzip > "${BACKUP_FILE}"
     
     # Encrypt backup file
     gpg --output "${BACKUP_FILE}.gpg" --encrypt "${BACKUP_FILE}"
     
     # Transfer encrypted backup file to remote storage
     scp "${BACKUP_FILE}.gpg" user@remote-server:/path/to/storage
     ```

These script-level answers demonstrate practical implementations for each scenario, covering tasks such as backup creation, disk monitoring, user provisioning, log parsing, and database backups.

6. **Monitoring CPU usage on a Linux server**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Define CPU usage threshold
     THRESHOLD="90"  # Adjust as needed
     
     # Get CPU usage percentage
     CPU_USAGE=$(top -bn1 | grep "Cpu(s)" | awk '{print $2}' | cut -d'%' -f1)
     
     # Check if CPU usage exceeds threshold and send alert
     if [ "${CPU_USAGE}" -gt "${THRESHOLD}" ]; then
         mail -s "High CPU Usage Alert" admin@example.com <<< "CPU usage is ${CPU_USAGE}%"
     fi
     ```

7. **Automating log rotation for Apache access logs**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Define log file and rotation parameters
     LOG_FILE="/var/log/apache2/access.log"
     ROTATE_SIZE="100M"
     KEEP_COUNT="5"
     
     # Rotate log file if it exceeds size threshold
     if [ "$(du -m "${LOG_FILE}" | cut -f1)" -gt "${ROTATE_SIZE%%M*}" ]; then
         mv "${LOG_FILE}" "${LOG_FILE}.$(date +"%Y%m%d%H%M%S")"
         systemctl restart apache2
     fi
     
     # Delete old log files to keep count within limit
     ls -t "${LOG_FILE}".* | tail -n +${KEEP_COUNT} | xargs rm -f
     ```

8. **Automating SSL certificate renewal for Nginx server**:
   - Script:
     ```bash
     #!/bin/bash
     
     # Define SSL certificate directory and renewal command
     CERT_DIR="/etc/nginx/ssl"
     RENEW_CMD="certbot renew --nginx"
     
     # Run certificate renewal command and reload Nginx
     ${RENEW_CMD} && systemctl reload nginx
     ```

9. **Extracting data from CSV files using Python script**:
   - Script:
     ```python
     #!/usr/bin/env python3
     
     import csv
     
     # Define input CSV file and output data structure
     CSV_FILE = 'input.csv'
     data = {}
     
     # Read CSV file and count occurrences of each value in column 2
     with open(CSV_FILE, newline='') as csvfile:
         reader = csv.reader(csvfile)
         for row in reader:
             value = row[1]
             if value in data:
                 data[value] += 1
             else:
                 data[value] = 1
     
     # Output results
     print(data)
     ```

10. **Automating file synchronization between two servers using rsync**:
    - Script:
      ```bash
      #!/bin/bash
     
      # Define source and destination directories
      SOURCE_DIR="/path/to/source"
      DEST_DIR="user@remote-server:/path/to/destination"
     
      # Synchronize files from source to destination
      rsync -avz --delete "${SOURCE_DIR}/" "${DEST_DIR}/"
      ```

11. **Automating database backups using a bash script**:
    - Script:
      ```bash
      #!/bin/bash
     
      # Define database credentials and backup directory
      DB_USER="username"
      DB_PASS="password"
      DB_NAME="database_name"
      BACKUP_DIR="/path/to/backups"
     
      # Create backup filename with timestamp
      BACKUP_FILE="${BACKUP_DIR}/${DB_NAME}-$(date +%Y%m%d%H%M%S).sql"
     
      # Dump database to backup file
      mysqldump -u${DB_USER} -p${DB_PASS} ${DB_NAME} > ${BACKUP_FILE}
     
      # Optionally compress backup file
      gzip ${BACKUP_FILE}
      ```

12. **Monitoring disk space usage on a Linux server**:
    - Script:
      ```bash
      #!/bin/bash
     
      # Define disk usage threshold
      THRESHOLD="90"  # Adjust as needed
     
      # Get disk usage percentage
      DISK_USAGE=$(df -h / | awk 'NR==2 {print $5}' | cut -d'%' -f1)
     
      # Check if disk usage exceeds threshold and send alert
      if [ "${DISK_USAGE}" -gt "${THRESHOLD}" ]; then
          mail -s "High Disk Usage Alert" admin@example.com <<< "Disk usage is ${DISK_USAGE}%"
      fi
      ```

13. **Automating website availability monitoring using curl**:
    - Script:
      ```bash
      #!/bin/bash
     
      # Define website URL
      WEBSITE_URL="https://example.com"
     
      # Check website availability
      if curl --output /dev/null --silent --head --fail "${WEBSITE_URL}"; then
          echo "Website is UP"
      else
          echo "Website is DOWN"
          # Optionally send alert
      fi
      ```

14. **Generating a random password using a Python script**:
    - Script:
      ```python
      #!/usr/bin/env python3
     
      import random
      import string
     
      # Define password length and character set
      PASSWORD_LENGTH = 12
      CHARACTER_SET = string.ascii_letters + string.digits + string.punctuation
     
      # Generate random password
      password = ''.join(random.choice(CHARACTER_SET) for _ in range(PASSWORD_LENGTH))
     
      # Output generated password
      print(password)
      ```

15. **Automating file archival and compression using tar**:
    - Script:
      ```bash
      #!/bin/bash
     
      # Define source directory and output filename
      SOURCE_DIR="/path/to/files"
      OUTPUT_FILE="/path/to/archive.tar.gz"
     
      # Create tar archive and compress
      tar -czf "${OUTPUT_FILE}" "${SOURCE_DIR}"
      ```

16. **Script to automate user account management**:

```bash
#!/bin/bash

# Set username
USERNAME="newuser"

# Create user with home directory and specified shell
useradd -m -s /bin/bash ${USERNAME}

# Set initial password for user
echo "${USERNAME}:newpassword" | chpasswd


17. **Script to change the password for one member out of three with the same password**:
```bash
#!/bin/bash

# Assuming passwords are stored in an array
passwords=("password1" "password2" "password1")
passwords[2]="new_password"
```

18. **Script to push a repository and build a job in Jenkins**:
```bash
#!/bin/bash

git push origin master
curl -X POST http://jenkins-url/job/job-name/build
```

19. **Explanation of EC2 and VPC with a script to create them using AWS CLI**:
EC2 (Elastic Compute Cloud) is a web service that provides resizable compute capacity in the cloud, and VPC (Virtual Private Cloud) is a virtual network dedicated to your AWS account. Below is a basic script to create an EC2 instance and VPC using AWS CLI:
```bash
#!/bin/bash

# Create EC2 instance
aws ec2 run-instances --image-id ami-123456 --instance-type t2.micro --key-name my-key --security-group-ids sg-123456

# Create VPC
aws ec2 create-vpc --cidr-block 10.0.0.0/16
```
20. **Script to monitor disk space and send email alerts**:
```bash
#!/bin/bash

# Set threshold for disk usage (in percentage)
THRESHOLD=90

# Get current disk usage
DISK_USAGE=$(df -h / | awk 'NR==2 {print $5}' | sed 's/%//')

# Check if disk usage exceeds threshold
if [ $DISK_USAGE -gt $THRESHOLD ]; then
    # Send email alert
    echo "Disk usage on server exceeds ${THRESHOLD}%" | mail -s "Disk Alert" user@example.com
fi
```

21. **Script to automate system updates using yum**:
```bash
#!/bin/bash

# Update system packages
yum -y update
```

22. **Script to automate file transfers using rsync**:
```bash
#!/bin/bash

# Set source and destination directories
SOURCE_DIR="/path/to/source"
DEST_DIR="/path/to/destination"

# Sync files from source to destination
rsync -avz ${SOURCE_DIR} ${DEST_DIR}
```

23. **Script to automate log rotation**:
```bash
#!/bin/bash

# Set log file and rotation threshold
LOG_FILE="/path/to/logfile.log"
THRESHOLD=1000000 # 1 MB

# Check if log file size exceeds threshold
if [ $(stat -c %s ${LOG_FILE}) -gt $THRESHOLD ]; then
    # Rotate log file
    mv ${LOG_FILE} ${LOG_FILE}.old
    # Create new empty log file
    touch ${LOG_FILE}
fi
```
24. a simple Bash script that checks whether a file exists in a directory:

```bash
#!/bin/bash

# Define the directory path and filename
directory="/path/to/directory"
filename="example.txt"

# Check if the file exists
if [ -e "$directory/$filename" ]; then
    echo "File $filename exists in $directory"
else
    echo "File $filename does not exist in $directory"
fi
```

```
25. **Script to backup MySQL databases**:
```bash
#!/bin/bash

# Set backup directory
BACKUP_DIR="/path/to/backup"

# Set MySQL credentials
DB_USER="username"
DB_PASSWORD="password"

# Get list of databases
DATABASES=$(mysql -u${DB_USER} -p${DB_PASSWORD} -e "SHOW DATABASES;" | grep -Ev "(Database|information_schema|performance_schema)")

# Loop through each database and backup
for DB in $DATABASES; do
    mysqldump -u${DB_USER} -p${DB_PASSWORD} ${DB} > ${BACKUP_DIR}/${DB}.sql
done
```

26. **Script to monitor CPU usage and send alerts**:
```bash
#!/bin/bash

# Set threshold for CPU usage (in percentage)
THRESHOLD=80

# Get current CPU usage
CPU_USAGE=$(top -bn1 | grep "Cpu(s)" | awk '{print $2}' | cut -d. -f1)

# Check if CPU usage exceeds threshold
if [ $CPU_USAGE -gt $THRESHOLD ]; then
    # Send email alert
    echo "CPU usage on server exceeds ${THRESHOLD}%" | mail -s "CPU Alert" user@example.com
fi
```

27. **Script to automate website uptime monitoring**:
```bash
#!/bin/bash

# Set website URL
URL="https://example.com"

# Perform HTTP request and check status code
STATUS_CODE=$(curl -s -o /dev/null -w "%{http_code}" ${URL})

# Check if website is down (status code not equal to 200)
if [ ${STATUS_CODE} -ne 200 ]; then
    # Send email alert
    echo "Website ${URL} is down (HTTP status code: ${STATUS_CODE})" | mail -s "Website Alert" user@example.com
fi
```

28. **Script to automate SSL certificate expiration checks**:
```bash
#!/bin/bash

# Set SSL certificate file
CERT_FILE="/path/to/certificate.crt"

# Get expiration date of SSL certificate
EXPIRATION_DATE=$(openssl x509 -enddate -noout -in ${CERT_FILE} | cut -d= -f2)

# Convert expiration date to timestamp
EXPIRATION_TIMESTAMP=$(date -d "${EXPIRATION_DATE}" +%s)

# Get current timestamp
CURRENT_TIMESTAMP=$(date +%s)

# Calculate number of days until expiration
DAYS_LEFT=$(( (${EXPIRATION_TIMESTAMP} - ${CURRENT_TIMESTAMP}) / 86400 ))

# Check if SSL certificate is expiring soon (e.g., within 30 days)
if [ ${DAYS_LEFT} -lt 30 ]; then
    # Send email alert
    echo "SSL certificate will expire in ${DAYS_LEFT} days" | mail -s "SSL Certificate Alert" user@example.com
fi
```

29. **Script to automate backup of configuration files**:
```bash
#!/bin/bash

# Set directory containing configuration files
CONFIG_DIR="/etc"

# Set backup directory
BACKUP_DIR="/path/to/backup"

# Backup each configuration file
for FILE in ${CONFIG_DIR}/*; do
    cp ${FILE} ${BACKUP_DIR}
done
```

30. **Script to automate cleanup of temporary files**:
```bash
#!/bin/bash

# Set directory containing temporary files
TMP_DIR="/tmp"

# Remove temporary files older than 7 days
find ${TMP_DIR} -type f -mtime +7 -exec rm -f {} \;
```

These additional scripts cover various automation scenarios such as MySQL database backups, CPU usage monitoring, website uptime checks, SSL certificate expiration checks, configuration file backups, and cleanup of temporary files.
