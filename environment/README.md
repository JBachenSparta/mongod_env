# README file for DEVELOPMENT environment

From GitHub clone this repository down to your local host
```bash
git clone git@github.com:JBachenSparta/dev_environments.git
```

Within the terminal navigate into the DevEnvionments folder, in the command line run:

```bash
cd dev_environments
```

Within terminal run the command:
```bash
vagrant up
```

Then navigate to:
- http://development.local:3000/

You should see:
- "The app is running correctly.
Welcome to the Sparta Test App"

Your development environment is now up and running, within here you can build and test your code. 


When the command 'vagrant up' is executed a bash script within provision.sh is triggered which executes the a series of commands automatically.


```bash
sudo apt-get update -y
```
Will identify what packagaes and repositories can be updated

```bash
sudo apt-get upgrade -y
```
Will fetch any updates identified by apt-get update and install them.

```bash
sudo apt-get install nginx -y
```
Install nginx

```bash
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
```
curl is a command line to transfer data, in this case from the link, whilst |sudo -E bash - takes the data from the link and runs it on the command line

```bash
sudo apt-get install nodejs -y
```
Will install nodejs

```bash
sudo npm install -g pm2
```
Installs pm2, process manager, through NPM, node package manager

```bash
cd /app
```
current directory level look for depository 'app'


```bash
pm2 start app.js
```
process manager runs app.js

app.js is listening to port 3000 so we must use the URL http://development.local:3000/ to access our environment
