# Step 1: Creating an organization in GitHub
**Create an organization:**  

   - Log in to GitHub.  
   - Select the "Create an organization" menu.
   ![Create a new organization.png](image/Project%20Setup/Create%20an%20organization%20in%20Github/Create%20a%20new%20organization.png)

**Select a pricing plan:**  

   - Choose an appropriate pricing plan for your organization.
   ![Free ogranization.png](image/Project%20Setup/Create%20an%20organization%20in%20Github/Free%20ogranization.png)

**Set up the organization:**  

   - Fill in the necessary settings.  
   ![Set up your organization.png](image/Project%20Setup/Create%20an%20organization%20in%20Github/Set%20up%20your%20organization.png)
   - Confirm the creation.  
   
   ➤ The URL of your future site will be generated from the "Organization name" field and will follow this structure: https://[site-name].github.io/.

# Step 2: Create a new repository
**Create a repository:**

![New repo.png](image/Project%20Setup/Create%20a%20new%20repository/New%20repo.png)
   ➤ Create a repository on behalf of the organization.  
   ➤ Select public/empty (the repository should not contain, for example, README.md).
![a new repository config.png](image/Project%20Setup/Create%20a%20new%20repository/a%20new%20repository%20config.png)
**Clone the repository in PyCharm:**

   - Copy the repository URL (either HTTPS or [SSH](# "Secure Shell: a protocol for securely connecting to remote servers, often used to work with repositories. Requires SSH keys to be configured.")).
   - In PyCharm, select "[Clone Repository](# "The process of copying a remote repository from GitHub to a local computer for working with it")" or "[Get from VCS](# "The process of copying a remote repository from GitHub to a local computer for working with it")".
   ![Get from VCS.png](image/Project%20Setup/Create%20a%20new%20repository/Get%20from%20VCS.png)
   - Copy the URL from your organization's page in GitHub (I choose SSH).
   ![SSH Url.png](image/Project%20Setup/Create%20a%20new%20repository/SSH%20Url.png)
   - Paste the URL and click "Clone".

   ➤ If you choose [SSH](# "Secure Shell: a protocol for securely connecting to remote servers, often used to work with repositories. Requires SSH keys to be configured."), make sure you have [SSH](# "Secure Shell: a protocol for securely connecting to remote servers, often used to work with repositories. Requires SSH keys to be configured.") settings configured. We'll discuss why this is more convenient in later posts.  

   - Click “Trust Project” in the window that opens.
# Step 3: Setting up a virtual environment
**Create a virtual environment:**

   - Run the following command in the [PyCharm](# "Integrated development environment (IDE) with support for Python, Markdown files, and documentation preview functions") [terminal](# "A program for executing commands in the text interface of the operating system"):
   ![python -m venv venv.png](image/Project%20Setup/Setting%20up%20a%20virtual%20environment/python%20-m%20venv%20venv.png)
     ```
     python -m venv .venv
     ```

➤ If you get a "command not found" error, check your installed Python version and adjust the command accordingly.  

   ![venv -not found.png](image/Project%20Setup/Setting%20up%20a%20virtual%20environment/venv%20-not%20found.png)
   Your Python version:  
   ![Python version.png](image/Project%20Setup/Setting%20up%20a%20virtual%20environment/Python%20version.png)
   For example, I used:
   ```
   python3.13 -m venv .venv
   ```

➤ You can see the [PyCharm](# "Integrated development environment (IDE) with support for Python, Markdown files, and documentation preview functions") version in the lower right corner of the screen.  
➤ Setting up a virtual environment helps avoid conflicts between packages in different projects.  
➤ It's not possible to install two or more different versions of the same package in one environment. The solution is to create another environment.

**Activate the environment:**

   - In the [PyCharm](# "Integrated development environment (IDE) with support for Python, Markdown files, and documentation preview functions") [terminal](# "A program for executing commands in the text interface of the operating system"), run:
     ```source .venv/bin/activate```
     
# Step 4: Install MkDocs and the necessary packages
**Install via [pip](# "A tool for installing and managing Python libraries and packages"):**

   - Run the following in the [terminal](# "A program for executing commands in the text interface of the operating system"): ```pip install mkdocs mkdocs-material```

➤ If needed, specify the version with: ```pip3.13 install mkdocs mkdocs-material```

   - Alternatively, use the "Packages" toolbar in [PyCharm](# "Integrated development environment (IDE) with support for Python, Markdown files, and documentation preview functions").


