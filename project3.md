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


Thereafter, I opened port 5000 from my EC2 Instance, as shown below:

![Opening Port 5000 in EC2 Instance](./images/opening-up-port-5000.PNG "Opening Port 5000 in EC2 Instance")


Then, I opened up my browser to access my server’s Public IP or Public DNS name followed by port 5000. The outcome is displayed below:

![Port Opened In Browser](./images/Port%20opened%20in%20browser.PNG "Port Opened In Browser")



---
 ### **CREATING ROUTES**
---



First, I created a folder called **routes** with the command below:

`mkdir routes`

Then I changed directory into the newly created directory, and then created an new file with the command below:


`touch api.js`

I opened the file with the Vim text editor and pasted in the code, as displayed below:

![api_js_file](./images/api-file.PNG)

Then, I saved the file


---
 ### **CREATING MODEL**
 ---

 First, I installed the mongoose, using the command:

 `npm install mongoose`

 Then I created a new faolder named '**models**' and changed directory into this newly-created folder.

 Thereafter, I created a file named **'todo.js'**

 I then opened this file in Vim and pasted the code in it, as shown below:

 ![](./images/todojs-file.PNG)

 After this, I saved the file.


Next, I updated the **'api.js'** file by replacing the code inside with the one displayed below:

![](./images/updated-route.PNG)

This file was then saved and exited.

---
### **MONGODB DATABASE**
---

I signed up for a shared clusters free account on mongoDB and the completed get-started checklist is displayed below:

![](./images/mongoDB.PNG)

