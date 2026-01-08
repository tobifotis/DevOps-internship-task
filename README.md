# DevOps Internship Tasks – Tyler Technologies

This repository contains tasks completed as part of my winter internship as a Junior DevOps Engineer at Tyler Technologies.

---

# [Task 1: Git & GitHub](https://github.com/tobifotis/DevOps-internship-task/tree/main/Git-Github)

**Objective**  
Gain hands-on experience with Git and GitHub fundamentals, including branching, commits, pull requests, and repository management.

**Reference**  
- Git Documentation: https://git-scm.com/doc

---

## Tasks:

1. Create a GitHub account.
2. Create a new GitHub repository.
3. Create a `Task1` folder in the `main` branch and add `Task1/README.md` file.
4. Create a `dev` branch, then create and push a test file.
5. Create a feature branch named `%USERNAME-new_feature`
6. Add a `README.md` file to the feature branch.
7. Verify repository status using `git status`.
8. Add a `.gitignore` file to ignore files starting with `.`
9. Commit and push changes to GitHub.
10. Open a Pull Request to merge the feature branch into the `dev` branch.
11. Merge `dev` into `main` via Pull Request.
12. Modify `README.md` in the feature branch, commit the change, and revert the last commit.
13. Generate a `git log` and save the output to `log.txt` in the `main` branch.
14. Delete the local and remote feature branch.
15. Document all Git commands used in `git_commands.md` (in the `dev` branch).
16. Share the repository link with the mentor.

---

# [Task 2: Linux Fundamentals](https://github.com/tobifotis/DevOps-internship-task/tree/main/Linux)

**Objective**  
Develop a solid foundation in Linux command-line usage, including navigation, file and directory management, permissions awareness, wildcards, and safe deletion practices.

**Reference**  
- Linux Command Line Basics: https://linuxcommand.org  
- Ubuntu Man Pages: https://manpages.ubuntu.com/

---

## Tasks:

### 🔹Understanding the Linux Environment

1. Open the terminal.
2. Display the current working directory using `pwd`.
3. List directory contents using `ls`.
4. View detailed file information using `ls -l`.
5. Display hidden files using `ls -a`.
6. Combine flags using `ls -la`.
7. Clear the terminal using `clear`.
8. View command history using `history`.

---

### 🔹Navigating the File System

9. Navigate to the root directory using `cd /`.
10. List top-level system directories.
11. Navigate into `/home` and list users.
12. Navigate into your user directory (`admin`).
13. Return to your home directory using `cd ~`.
14. Navigate into the `Documents/` directory.

---

### 🔹Creating Directories and Files

15. Create two directories:
    - `Folder1`
    - `Folder2`
16. Verify directory creation using `ls`.
17. Create text files using `touch`:
    - `bale.txt`
    - `ball.txt`
    - `bowl.txt`
    - `bull.txt`
18. Verify file creation using `ls`.

---

### 🔹Moving Files and Using Wildcards

19. Move `bale.txt` into `Folder1`.
20. Move `ball.txt` into `Folder1`.
21. Verify remaining files in `Documents/`.
22. Move all `.txt` files into `Folder2` using `*.txt`.
23. Confirm only directories remain in `Documents/`.

---

### 🔹Absolute, Relative, and Home Paths

24. Change directory into `Folder1`.
25. List files inside `Folder1`.
26. List files in `Folder2` using:
    - Absolute path (`/home/admin/Documents/Folder2`)
    - Home shortcut (`~/Documents/Folder2`)
    - Relative path (`../Folder2`)

---

### 🔹Hidden Files and Permissions

27. Create a hidden file using `touch .balehidden.txt`.
28. Display hidden files using `ls -la`.
29. Observe file permissions and ownership.
30. Understand the meaning of `r`, `w`, and `x` permission flags.

---

### 🔹Wildcard Pattern Matching

31. Use `?` to match filenames of equal length (example: `b??l.txt`).
32. Use bracket patterns to match specific characters (example: `b[ao][wl]l.txt`).
33. Verify matched files using `ls`.

---

### 🔹Removing and Renaming Directories

34. Create a new directory `Folder3`.
35. Rename `Folder3` to `Jason` using `mv`.
36. Remove the empty directory using `rmdir`.
37. Attempt to remove a non-empty directory using `rmdir` and observe the error.
38. Remove a directory and its contents using `rm -r`.

---

### 🔹Verification and Cleanup

39. Verify final directory state using `ls`.
40. Return to the home directory using `cd ~`.

---

# [Task 3: AWS]()
**Objective**  
Establish a secure AWS account foundation following best practices, configure IAM access, set up the AWS CLI, and launch, access, and clean up a test EC2 instance using both console-based and SSH-based methods.

**Reference**  
- AWS Account Setup: https://www.youtube.com/watch?v=CjKhQoYeR4Q&t=105s 
- AWS Services Explained: https://www.youtube.com/watch?v=JIbIYCM48to

---

## Tasks

### 🔹Root Account Security & Billing Setup
1. Create an AWS account.
2. Sign in as the root user.
3. Enable Multi-Factor Authentication (MFA) for the root user.
4. Configure billing information and payment method.
5. Set up billing alerts and cost monitoring.

---

### 🔹IAM Admin User Setup
6. Create an IAM admin user.
7. Attach the `AdministratorAccess` policy to the admin user.
8. Enable MFA for the IAM admin user.
9. Sign out from the root user.
10. Sign in using the IAM admin account.

---

### 🔹AWS CLI Installation & Configuration
11. Install the AWS CLI on the local machine.
12. Configure the AWS CLI using the IAM admin user’s access keys:
   ```bash
   aws configure
   ```
13. Verify CLI authentication:
   ```bash
   aws sts get-caller-identity
   ```

---

### 🔹EC2 Instance Creation
14. Create a test EC2 instance using the AWS Management Console.
15. Generate and download an EC2 key pair (`.pem` file).
16. Configure a security group allowing SSH access (port 22).
17. Launch the EC2 instance.

---

### 🔹Connecting to EC2
18. Connect to the instance using EC2 Instance Connect.
19. Connect to the instance using an SSH client:
   ```bash
   ssh -i <keypair>.pem ec2-user@<public-ip>
   ```
20. Verify successful login and basic shell access.

---

### 🔹Cleanup & Cost Management
21. Exit the EC2 instance.
22. Terminate the EC2 instance.
23. Confirm that no running EC2 resources remain.

---

## Note!
- The root account is used **only** for billing and account-level configuration.
- All operational tasks are performed using an IAM admin user.
- All resources are terminated to avoid unnecessary costs.
