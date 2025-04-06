## 1. On GitHub Page: Create a New Repository
- Go to [GitHub](https://github.com).
    
- Click on the **Repositories** tab in your profile.
    
- Click on the **New** button to create a new repository.
    
- Fill in the following details:
    
    - **Repository name**: Choose a name for your repository.
        
    - **Description**: Optionally, add a short description of the repository.
        
    - **Visibility**: Choose whether the repository should be **public** or **private**.
        
    - Optionally, initialize the repository with a README file if you want.
        
- Once you've filled in the details, click on **Create repository**.

### Tips:
- **Avoid using spaces in your file names**: Spaces in file names can sometimes cause issues with version control and scripting. Instead of spaces, consider using hyphens (`-`) or underscores (`_`) to separate words.
- **Use Markdown grammar**: When writing documentation or notes, ensure you use proper **Markdown syntax** to format your text. For example, use `#` for headings, `**bold**` for emphasis, and `*italic*` for styling.
  
### 2. **Add a File (Simple Markdown or Code File)**

- If your file is simple (like a markdown or code file), you can directly go to the "Add file" option and either:
    
    - **Create a new file** (by typing or pasting content).
        
    - **Upload an existing file** from your computer.
- If your file is more complex or requires many changes over time, it might be better to clone the repository locally to your computer, make the changes, and then push those changes back to GitHub. Let's go to **step 3**.
## 3. Open **Terminal**: Clone GitHub Repository to Your Local Address
- Open your terminal (on Windows, this could be Command Prompt or PowerShell, on macOS or Linux, just the Terminal).
- Clone your repository by running the following command:
```
[your computer] ~%cd [your/path]
```

```bash
git clone https://github.com/your-username/your-repository.git
```

- This will create a local copy of your repository on your computer.
## 4. Open **VSCode**:

### 4.1 Open Terminal in VSCode

- Open VSCode.
    
- Open the terminal inside VSCode by pressing **Ctrl + Shift + ~(tilde)
    
### 4.2 Add Changes

- about preparing changes:
    `git add . `
	- **Note**: The `.` (dot) in `git add .` means "add all changes within the current directory and its subdirectories." It stages all modified files, newly created files, and deleted files for the next commit.
### 4.3 Commit Changes
- recording those changes in the version history:
	```git commit -m "Automated commit" ```
	
### 4.4 Check the Status

- To check the current status of your repository (whether files are staged for commit), run:
    `git status`

### 4.5 Push to GitHub

- Push your changes to GitHub with the following command:
    `git push`

### FAQ: Invalid Username or Password

- If you encounter an error such as "Invalid username or password," make sure to go to your [GitHub SSH and GPG keys settings](https://github.com/settings/keys).
    
- Add a new SSH key by following the instructions on that page. After this, you'll be able to authenticate via SSH instead of entering your username and password every time.
    

## 5. Automate Updates Using `update.sh`

- Create a shell script `update.sh` to simplify pushing changes.
    
    1. In your repository directory, create a new file called `update.sh`.
        
    2. Inside `update.sh`, add the following commands:
	```bash
        git add .
        git commit -m "Automated commit" 
        git push
    ```
        
     3. Save the file and give it execute permissions by running:
        `chmod +x update.sh`
        
    4. Now, every time you need to update and push changes, you can simply run:
        `./update.sh`
        

This will streamline your workflow and make updates more efficient.

## 6. Renew Your GitHub Repository

Every time you revise your files locally in **VSCode** and run `./update.sh`, your GitHub repository will be updated, and you can see the revision reflected on GitHub.


By following these tips, you will maintain a smoother workflow and ensure compatibility across different systems.


## 🔧 Most Useful Mac Shortcuts (for Coding)

### 💻 Editor (VS Code / general)

| Shortcut                      | Action                         |
|------------------------------|--------------------------------|
| `Cmd + /`                    | Toggle comment line            |
| `Cmd + D`                    | Select next matching word      |
| `Option + ↑ / ↓`             | Move current line up/down      |
| `Option + Shift + ↑ / ↓`     | Copy current line up/down      |
| `Cmd + Z`                    | Undo                           |
| `Cmd + Shift + Z`            | Redo                           |

### 🖥 Terminal

| Shortcut     | Action                           |
|--------------|----------------------------------|
| `↑`          | Use previous command             |
| `↓`          | Use next command                 |
| `Ctrl + C`   | Cancel current command           |
| `Ctrl + L`   | Clear screen (like `clear`)      |
| `Ctrl + R`   | Search command history           |




