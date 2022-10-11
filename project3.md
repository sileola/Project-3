# **PROJECT 3: MERN STACK IMPLEMENTATION**
___
### **STEP 1: BACKEND CONFIGURATION**
___

I ran the following commands on my virtual machine to update a list of packages in the Ubuntu package manager and to upgrade the Ubuntu OS:

`sudo apt update`

`sudo apt upgrade`

Next, I got the location of Node.js software from Ubuntu repositories by running the command below:

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

 Then I created a new folder named '**models**' and changed directory into this newly-created folder.

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

Next, in the ToDo directory, I created a file called **.env**, using the command below:

`touch .env`

I opened the file up using vim and I added the connection string to access the database in it, as below:

![](./images/connection-string.PNG)

Next, I updated the **index.js** file with a different code, shown below:

![](./images/updated-indexjs-file.PNG)

I started the server using the command:

`node index.js`

The result is shown below:

![Connected Database](./images/connected-database.PNG "Connected Database")

---
### **Testing Backend Code without Frontend using RESTful API**
---

I installed **Postman**, created a ***POST*** request and set it up as displayed below:

![](./images/postman1.PNG)

![](./images/postman2.PNG)

After this, I sent the request and the response is shown below:

![POST Request](./images/POST-REQUEST.PNG "POST Request")

Thereafter, I set-up the ***GET*** request and on sending it, the output is shown below:

![GET Request](./images/GET-request.PNG "GET Request")

### **Optional Task:** To Create **DELETE** request:

I set my request up with its ID 

![DELETE Request](./images/DELETE-REQUEST.PNG "DELETE Request")


___
### **STEP 2: FRONTEND CREATION**
___

First, I cd into the ToDo directory and then ran this command:

`npx create-react-app client`



### **Running a React App**
Before testing the react app, I installed the following dependencies dependencies:

1. To run more than one command simultaneously from the same terminal window, I installed **Concurrently** using the command below:

`npm install concurrently --save-dev`

The output is displayed below:

![Concurrently Installation](./images/concurrently-installation.PNG "Concurrently Installation")

2. Next, I installed **Nodemon** using the command below:

`npm install nodemon --save-dev`

The output is shown below:

![Nodemon Installation](./images/Nodemon-installation.PNG "Nodemon Installation")

Next, I opened the **packet.json** file and I updated the needed part as shown below:


![](./images/updated-package-json.PNG)


### **Configuring Proxy in the package.json**

First, I cd in the 'client' directory

Next, I opened the package.json file in Vim and I added the proxy configuration, as shown below:

![](./images/proxy-config.PNG)


Next, I cd into the 'ToDo' directory and I ran the following command:

`npm run dev`

Next, I opened TCP port 3000 on my EC2 and I could access it over the internet. The output is displayed below:


![](./images/react.PNG)



### **Creating The React Components**

First, I cd 'client' then I cd to 'src'

Next, I created another folder called 'compoments' by running the command below:

`mkdir components`

Then I cd into the newly created 'compoments' directory and created three new files 'Input.js', 'ListTodo.js' and 'Todo.js.', by running the command below:

`touch Input.js ListTodo.js Todo.js`


Next, I opened Input.js file in Vim


I pasted in the code provided and saved it, as shown below:

![](./images/input-js.PNG)

I the cd into 'client' folder and run the followin command to install **Axios**:

`npm install axios`



Next, from the ‘components’ directory, I opened the **ListTodo.js** file with Vim and pasted and saved into it the code provided, as shown below:

![](./images/list-js.PNG)



Next, also from the ‘components’ directory, I opened the **Todo.js** file with Vim and pasted and saved into it the code provided, as shown below:

![](./images/todo-js.PNG)

Next, I cd to 'src' folder then I opened the 'App.js' file in Vim. I then pasted and saved into it the code provide, as shown below:

![](./images/App-js-file.PNG)


Next, from the same 'src' folder I opened the 'App.css' file in Vim. I then pasted and saved into it the code provide, as shown below:


![](./images/app-css-file.PNG)

Next, also in the same 'src' folder I opened the 'index.css' file in Vim. I then pasted and saved into it the code provide, as shown below:

![](./images/index-css-file.PNG)

I then moved to the 'ToDo' directory and ran the following command:

`npm run dev`

My To-Do App is now fully functional and it is interactive. This is displayed below:

![My To-Do App](./images/MyToDo.PNG) "My To-Do App")