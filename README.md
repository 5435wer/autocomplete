Here is the (_hopefully_) super simple guide to installing the Sparx Autocompleter client on different platforms.
Tutorial:https://www.youtube.com/watch?v=cPtYj4sWg74

# Windows

Each step will include a video demonstrating the text instructions for visual learners or those who prefer video guides (WIP).

## 1. Installing Git

First, you need to install Git. This allows you to clone the repository to your drive.

### Via the installer

Visit the [Git for Windows download page](https://git-scm.com/downloads/win) and download the installer that matches your version of Windows.

Under "Standalone Installer", download either the 32-bit or 64-bit Git for Windows Setup, depending on your system. ([How to tell if my PC is 32-bit or 64-bit?](https://youtu.be/GvRdU_mHBcU))

Once it has downloaded, run it and it will guide you through the setup process.

**IMPORTANT**: Make sure to select "Git from the command line and also 3rd-party software" when installing. This is so that you can use the command prompt to clone directories.

### Via WinGet

Open Powershell and type the following:
```
winget install --id Git.Git -e --source winget
```

Press "Yes" on the User Account Control prompt and wait until the setup finishes.

The Powershell window should output "Successfully installed"

## 2. Installing Node.js

Now you need to install Node.js. This provides npm, a JavaScript package manager. It also lets you run the Sparx Autocompleter.

### Via the installer

Go to the [Node.js site](https://nodejs.org/en). It should have a large button saying "Download Node.js (LTS)".

Click it to download (the appropriate version for your system, such as 32-bit or 64-bit, should be selected automatically).

Once it has downloaded, run it and it will guide you through the setup process.

**IMPORTANT**: Make sure to select "Add to PATH" when installing. This is so that you can use Node.js on command prompt without configuration.

## 3. Installing Sparx Autocompleter

Open a new command prompt (cmd) window.

Use the ```cd``` command to navigate to the directory where you want to clone the autocompleter. (e.g. ```cd C:\Users\username\Documents```)

Now, clone the repository using the command: 
```
git clone https://github.com/woody-willis/sparx-autocompleter
```

Once completed, navigate to the cloned repository using the command: 
```
cd sparx-autocompleter
```

Now, install dependencies for the autocompleter using the command: 
```
npm install
```

## 4. Setting up the .env

Find the file named ```.env``` in the directory ```sparx-autocompleter``` which you cloned earlier.

Open it with your text editor of choice.

### Adding Sparx credentials

Enter your Sparx details between the quotes ("") of this text (in ```.env```):

```
SPARX_SCHOOL=""
SPARX_USERNAME=""
SPARX_PASSWORD=""
```

The school name should ideally be exact, but the autocompleter can search for near matches.

**IMPORTANT**: Microsoft and Google accounts currently do not work, this is for Sparx accounts only!

### Adding a Gemini API key

Go to the [Google AI Studio "Get an API key" page](https://aistudio.google.com/app/apikey).

Press "Create API key" and select a project.

You should get an API key that looks like ```AIzaSy*****```.

Press "Copy" and paste it in between the quotes ("") of this text (in ```.env```):

```
GEMINI_API_KEY=""
```

### Adding a DataImpulse API key (optional)

Go to [DataImpulse](https://dataimpulse.com/).

Add a new plan and purchase a residential proxy plan.

Go to "API Management" and press the copy button next to "API Token".

You should get an API key that looks like ```http://************.gb:***********@gw.dataimpulse.com```.

Remove the comment (#) and paste it in between the quotes ("") of this text (in ```.env```):

```
DATAIMPULSE_API_URL=""
```

## 5. Running Sparx Autocompleter

Use the ```cd``` command to navigate to the ```sparx-autocompleter``` directory. (e.g. ```cd C:\Users\username\Documents\sparx-autocompleter```)

Now use the command:
```
npm start
```

The Sparx Autocompleter should now be running successfully!

**Any time you need to use the program again, repeat step 5.**
