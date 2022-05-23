# **PROJECT 5: MERN STACK IMPLEMENTATION**
___
### **STEP 1: BACKEND CONFIGURATION**
___

I ran the following commands on my virtual machine to update a list of packages in the Ubuntu package manager and to upgrade the Ubuntu OS:

`sudo apt update`

`sudo apt upgrade`

Nex, I gott the location of Node.js software from Ubuntu repositories by running the command below:

`curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`

Next, to install Node.js on the server, I ran the command below:

`sudo apt-get install -y nodejs`

Thereafter, to verify the not installations, I ran the following commands:

`node -v `

`nmp -v`

The versions are shown in the image below

![Node and NPM Versions](./images/npm_and_node_versions.PNG "Node and NPM Versions")



---
 ### **APPLICATION CODE SET-UP**
 ---

 i first created a new directory for the project and named it ToDo, using the command below:

 `mkdir ToDo`

 I then changed directory into the new folder.

 Next, I ran the command `npm init` to initialise the project.

 The package.json file created is shown in the image below:

 ![Package json File](./images/package._json-file.PNG "Package json File")


---
 ### **INSTALLATION OF EXPRESSJS**
---

First, I installed **Express** using npm, by running the following command:

`npm install express`

I then proceeded to create the **index.js** file by running the command:

`touch index.js`

I also installed the **dotenv module** using the command:

`install dotenv`

The outcomes are shown below.

![Installations](./images/installations.PNG)


Thereafter, I opened the index.js file using vim and I pasted and saved the code provided into the file, shown below:

![](./images/code.PNG)

Next, I started the server on the terminal using the command below:

`mode index.js `

The outcome is shown below.

![Server Running on port 5000](./images/running-server.PNG "Server Running on port 5000")



