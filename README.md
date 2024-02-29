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

**
**Remember to run all terminal commands in the Ubuntu Terminal from now on.**
**

### ⚓️ Intro to Anchor 

Why Anchor?

1. **Simplicity:** Anchor is lightweight and easy to use, making it suitable for beginners who want to get started with web development without dealing with complex setups.
2. **Minimal Configuration:** Anchor requires minimal setup and configuration, allowing beginners to focus on learning HTML, CSS, and basic JavaScript concepts without the added complexity of tools and frameworks.
3. **Fast Results:** With Anchor, users can quickly build and deploy static websites, enabling them to see results and learn through hands-on experience without getting bogged down in technical details.

Install Anchor if you haven't already. You can do this via npm (Node Package Manager) by running the following command in your terminal or command prompt.

```
npm install -g anchor-cli
```

Use the `anchor init` command to create a new Anchor project. Navigate to the directory where you want to create your project and run the following command:

```
anchor init web_dev
```

Change into the directory of your newly created Anchor project:

```
cd web_dev
```

Within your project directory, create a new HTML file. You can do this using a text editor like VS Code, Sublime Text, or Notepad. Here's a simple example of an HTML file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Anchor Project</title>
</head>
<body>
    <h1>Hello, Anchor!</h1>
    <p>This is a super basic HTML webpage created using Anchor.</p>
</body>
</html>
```

After creating your HTML file, you can use Anchor to serve your website locally. Run the following command in your terminal:

```
anchor serve
```
