### 1.Project Workspace Setup
*Commands:* mkdir ~/documents
*Output:* No output returned by terminal but the command was executed succesfully.
*Explanation:* I created a new directory named documents in my home folder to serve as the intial storage area for project-related files.
*Screenshot:* ![Setup] (./screenshots/setup.png)

### 2.File Creation
*Commands:* cd ~/documents && touch plan.txt
*Output:* No output returned by terminal but the command was executed succesfully.
*Explanation:* I navigated into the newly created directory and used the touch command to initialize an empty file named plan.txt.
*Screenshot:* ![Create File] (./screenshots/create.png)

### 3.Content Addition
*Commands:* echo "This is a project reminder." > plan.txt
*Output:* No output returned by terminal but the command was executed succesfully.
*Explanation:* I wrote a shot project note into the plan.txt file using output redirection to demonstrate basic file editing. 
*Screenshot:* ![Add Content] (./screenshots/content.png)

### 4.File Metadata Verification
*Commands:* ls -l plan.txt
*Output:* -rw-r--r-- 1 shainee678 shainee678 28 Jan  1 10:56 plan.txt 
*Explanation:* I displayed the detailed listing of the file to verify its permissions, size, and that my username correctly appears as the owner.
*Screenshot:* ![Metadata] (./screenshots/metadata.png)

### 5.File Duplication
*Commands:* cp plan.txt plan_copy.txt
*Output:* No output returned by terminal but the command was executed succesfully.
*Explanation:* I created an exact duplicate of the project note and named it plan_copy.txt to test file copying operations.
*Screenshot:* ![Copy File] (./screenshots/copy.png)

### 6.Directory Renaming
*Commands:* mv ~/documents ~/projects_documents
*Output:* No output returned by terminal but the command was executed succesfully.
*Explanation:* I used the mv command to rename the entire documents folder to project_documents to better reflect the project's scope.
*Screenshot:* ![Rename Folder] (./screenshots/rename.png)

### 7.Archival Structure
*Commands:* mkdir ~/projects_documents/archive
*Output:* No output returned by terminal but the command was executed succesfully.
*Explanation:* I created a subdirectory to named archive inside the renamed project folder to organize older or duplicate files.
*Screenshot:* ![Archive Folder] (./screesnhots/archive_dir.png)

### 8.File Organization
*Commands:* mv ~/project_documents/plan_copy.txt ~/project_documents/archive
*Output:* No output returned by terminal but the command was executed succesfully.
*Explanation:* I moved the duplicate file in to the archive subdirectory to clean up the main project workspace.
*Screenshot:* ![Move File] (./screesnhots/move.png)

### 9.Recursive Listing
*Commands:* ls -R ~/project_documents
*Output:* /home/shainee678/project_documents:
archive  plan.txt  sample_data.txt  sample_hard.txt

/home/shainee678/project_documents/archive:
plan_copy.txt
*Explanation:* I performed a recursive list command to display the entire nested folder structure, showing both the main files and the archive contents.
*Screenshot:* ![Recursive List] (./screenshots/recursive.png)

### 10.Path Verification
*Commands:* readlink -f ~/project_documents/archive/plan_copy.txt
*Output:* /home/shainee678/project_documents/archive/plan_copy.txt
*Explanation:* I used this command to display the absolute (full) path of the moved file to verify its final location on the system.
*Screenshot:* ![Path View] (./screenshots/path.png)
