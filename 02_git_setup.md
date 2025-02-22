# Git Installation & Setup

## Installing Git
Git can be installed on different operating systems using the following methods:

### Windows
1. Download Git from the official website: [Git for Windows](https://git-scm.com/downloads)
2. Run the installer and follow the default settings.
3. Verify installation using:
   ```sh
   git --version
   ```

### macOS
1. Install Git via Homebrew:
   ```sh
   brew install git
   ```
2. Verify installation using:
   ```sh
   git --version
   ```

### Linux (Ubuntu/Debian)
1. Install Git using APT:
   ```sh
   sudo apt update
   sudo apt install git
   ```
2. Verify installation using:
   ```sh
   git --version
   ```

### Linux (Fedora)
1. Install Git using DNF:
   ```sh
   sudo dnf install git
   ```
2. Verify installation using:
   ```sh
   git --version
   ```

## Configuring Git
Once Git is installed, set up your username and email:

```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Checking Configuration
To check your current Git configuration:
```sh
git config --list
```

## Setting Up SSH Keys (Optional for Remote Repositories)
1. Generate an SSH key:
   ```sh
   ssh-keygen -t rsa -b 4096 -C "your.email@example.com"
   ```
2. Add the key to the SSH agent:
   ```sh
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_rsa
   ```
3. Copy the SSH key and add it to GitHub/GitLab:
   ```sh
   cat ~/.ssh/id_rsa.pub
   ```

## Summary
You have now installed and configured Git. Next, let's proceed to [03_git_basics.md](./03_git_basics.md) to learn Git's fundamental commands.

