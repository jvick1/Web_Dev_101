# Web_Dev_101

This repo aims to provide an introduction to coding with CSS and JavaScript, focusing on creating responsive web pages through project-based learning.

In the **CSS section**, we'll work with IDs, classes, and divisions, text properties, image styling, and navigation rules. 
The **JavaScript section** covers foundational concepts like placement and output, progressing to variables, arithmetic operators, arrays, conditional statements, loops, events, and functions, enabling students to integrate dynamic client-side functionality into their web pages.

We'll leverage the Windows Subsystem for Linux (WSL) to create a Linux environment for Website development.

### 👩‍💻 Setup WSL.

To utilize WSL, open `cmd.exe` in Admin mode and execute the following command:

```bash
wsl --install
```

This command installs the required components, downloads the latest Linux kernel, sets WSL 2 as default, and installs a Linux distribution (Ubuntu by default). 

**Restart your computer after the installation.**

You'll have to make a UN & PW for the new Ubuntu terminal.

### 📀 Installing Node.js.
Access the Ubuntu Terminal by searching for "Ubuntu" in your Start menu. 

Follow [this guide](https://learn.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-wsl) or use these commands to install Node.js using nvm:

```
// Install Curl
sudo apt-get install curl

// Install NVM
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

// Restart Ubuntu Terminal

// Test if nvm exists - this will return "nvm" and not a version number if working correctly!
command -v nvm

// Install the latest version of Node.js
nvm install --lts
```

**Remember to run all terminal commands in the Ubuntu Terminal from now on.**

### Create a New React App:

Use the `create-react-app` tool to create a new React application. Open your terminal or command prompt and run the following command:

```
npx create-react-app web_dev
```

![image](https://github.com/jvick1/Web_Dev_101/assets/32043066/fd6b566b-c5e6-4ae2-9ad8-c303f66a41e7)

and then let's create a new project called web_dev

```
cd web_dev
```

Run the following command to start the development server and view your React app in the browser:

```
npm start
```

This command will automatically open your default web browser and serve your React app at `http://localhost:3000`. The `App` function returns JSX (JavaScript XML) which is HTML-like syntax within JavaScript code. Overall, JSX and HTML share many similarities, and JSX syntax closely resembles HTML, making it easy for developers familiar with HTML to transition to React development. However, JSX introduces some additional features and syntax changes to support dynamic content generation and integrate seamlessly with JavaScript.

![image](https://github.com/jvick1/Web_Dev_101/assets/32043066/42bc5a32-27cf-4ebe-8bdd-1ea8b7f5d6ba)

This is the set up of the code. Now we can start by learning more about CSS & JS. 
