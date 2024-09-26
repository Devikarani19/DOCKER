# Node Hello World
Simple node.js app that servers "A Monk in Cloud"

Great for testing simple deployments on Cloud

## Step 1: Install NodeJS and NPM using nvm
Install node version manager (nvm) by typing the following at the command line.
sudo yum install curl -y
```bash
sudo su -
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```
Activate nvm by typing the following at the command line.

```bash
# Source .bashrc
source ~/.bashrc

# Or create .bash_profile
touch ~/.bash_profile
nano ~/.bash_profile

# Add NVM lines to .bash_profile and save
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"

# Source the file to apply changes
source ~/.bash_profile
```

Use nvm to install the latest version of Node.js by typing the following at the command line.
```bash
nvm install node
```

Test that node and npm are installed and running correctly by typing the following at the terminal:

```bash
node -v
npm -v
```

## Step 2: Install Git and clone repository from GitHub
To install git, run below commands in the terminal window:

```bash

yum install git -y
```

Just to verify if system has git installed or not, please run below command in terminal:
```bash
git — version
```

This command will print the git version in the terminal.

Run below command to clone the code repository from Github:

```bash
git clone <url>
```

Get inside the directory and Install Packages

```bash
npm install
```

Start the application
To start the application, run the below command in the terminal:

```bash
npm start
```

