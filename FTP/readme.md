# Set up

This folder contains the scripts and set up instructions for connecting to a hosting provide using FTP, then deploying to Githug Pages (while syncing files with the remote FTP server). Modifications can be made to deploy a different location.

**Requirements**

- Hosting account access (A2, Hostgator, etc.)
- FTP credentials
  - FTP URL
  - Port
  - Username
  - Password
- FTP client (such as [Filezilla](https://filezilla-project.org/) or [CyberDuck](https://cyberduck.io/))
- Git FTP (see [overview](https://github.com/git-ftp/git-ftp) and [installation](https://github.com/git-ftp/git-ftp/blob/master/INSTALL.md))
---

### Steps 

1) Login to the hosting proider to access cPanel
2) Create a new FTP account from cPanel
  - Depending on the account's existing files, you'll likely want to set the directory access to the folder that links to `/public_html/` (e.g. `home/example.com/public_html/`)
3) Log in to the server via FileZilla or CyberDuck
4) Download all project files to a local project directory
5) Set up a new, local git repository then connect the local repository with Github
6) Copy the scripts found from the /scripts/ folder to your local directory, then modify the FTP URL found under `scripts/setup`
7) Run `scripts/setup` to save your FTP credentials
8) You can now run `scripts/deploy` to push to Github Pages