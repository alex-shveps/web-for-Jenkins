# Final Project

## 1. Project theme: Jenkins CI/CD process.

---
## 2. Motivation: Since my experience in DevOps practice is insignificant, I decided to do the deployment and update of the Web page on a remote server.

---
## 3. Relevant: Now this is an urgent task because it allows the developer to make changes in the project as quickly as possible and see the result.

---
## 4. Goals: Automate the process of code delivery from the developer to the server.

---
## 5. Task:

#### 1) Create an environment

#### 2) Set up working machines

#### 3) Deploy the web server

#### 4) Commit change to GitHub

#### 5) Deliver changes to a remote web server

---
## 6. Designing:

#### 1) Use 3 working machines: Windows(User), AWS_EC2_Jenkins, AWS_EC2_WebServer

#### 2) Use the GitHub repository to store our project, let's make it commit and push our project.

#### 3) Use Jenkins to manage and automate our work.

#### 4) Use AWS EC_2 service to create servers.

#### 5) Use Apache Web Server to deploy our html project.

---
## 7. Realization:

#### 1) Create repository on GitHub: "web-for-Jenkins"

#### 2) Create file our html page:

index.html
````html
<!DOCTYPE html>

<html>
    <head>
        <title>My CV V.1</title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div class="wrapper"></div>
        <h1 class="index">Cloud&DevOps Fundamentals Autumn 2022</h1> 
        <hr>
        <img src="IMG_6873.jpg" height="200"> 
        <br>
        <a href="https://github.com/alex-shveps/EPAM_Homework" target="_blank" >github repositories with home-task </a>
        <br>
        <a href="https://github.com/alex-shveps/EPAM_Homework" target="_blank" >github repositories with home-task </a>
        <br>
        <a href="https://drive.google.com/file/d/1bqw9WfrogYB7DXxvoCJPKF1ls4EwMwh6/view?usp=share_link" target="_blank"> My CV </a>
    </body>
</html>
````

style.css
````css
[href="https://github.com/alex-shveps/EPAM_Homework"] {
    color: rgb(0, 0, 0);
}

[href="https://drive.google.com/file/d/1bqw9WfrogYB7DXxvoCJPKF1ls4EwMwh6/view?usp=share_link"] {
    color: rgb(0, 0, 0);
}
body{
    background-color: rgb(74, 151, 151);
}
.wrapperERROR {
    width: 100;
    background-color: blue;
}

.index {
    text-align: center;
    color: rgb(229, 255, 0);
}

.error {
    text-align: center;
    color: rgb(255, 0, 0);
}
````

error.html
````html
<!DOCTYPE html>

<html>
    <head>
        <title>ERROR</title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div class="wrapperERROR"></div>
        <h1 class="error">ERROR</h1>
    </body>
</html>
````
add some picture
![](screnn/github_screen.png)


#### 3) Clone this repository on localhost(Windows):

use PowerShell
````
git clone git@github.com:alex-shveps/web-for-Jenkins.git
git status
````
![](screnn/windows_git_status.png)

#### 4) Create 2 EC_2 instance on AWS:

