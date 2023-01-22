## ELECRON BOLERPLATE - ELECTRON + PHP

This is a boilerplate for Electron + PHP

### How to use

1. Clone this repository

2. Install dependencies

```bash
npm install
```

3. Run the application

```bash
npm start
```

### How to build

```bash
npm run build
```

### How to build for Windows

```bash
npm run build:win
```

### How to build for Linux

```bash

npm run build:linux
```

### How to build for Mac

```bash

npm run build:mac
```

### How to build for all platforms

```bash

npm run build:all
```

### How to build for all platforms and publish

```bash

npm run build:all:publish
```

### How to build for all platforms and publish to Github

```bash

npm run build:all:publish:github
```

### How to build for all platforms and publish to S3

```bash

npm run build:all:publish:s3
```

HOW TO INSERT YOUR PHP CODE

1. Create a folder in the root of the project called "php"

2. Create a file called "index.php" in the folder "php"

3. Insert your PHP code in the file "index.php"

4. Run the application

```bash
npm start
```

5. Open the console and see the result of your PHP code

BULD AN ELECTRON APP

Electron is a framework for creating native applications with web technologies like JavaScript, HTML, and CSS. It takes care of the hard parts so you can focus on the core of your application.

To learn more about Electron and its API, please see the documentation.

### Prerequisites

- [Node.js](https://nodejs.org/en/) (v12.0.0 or newer)

### Quick Start

Clone this repository and install its dependencies:

```bash
git clone
cd electron-boilerplate-php
npm install
```

Then, you can run the app to see Electron in action:

```bash
npm start
```

### Documentation

- [Quick Start Guide](https://www.electronjs.org/docs/tutorial/quick-start)

- [Application Architecture](https://www.electronjs.org/docs/tutorial/application-architecture)

- [Using Native Node Modules](https://www.electronjs.org/docs/tutorial/using-native-node-modules)

- [Application Distribution](https://www.electronjs.org/docs/tutorial/application-distribution)

- [Mac App Store Submission Guide](https://www.electronjs.org/docs/tutorial/mac-app-store-submission-guide)

- [Windows Store Guide](https://www.electronjs.org/docs/tutorial/windows-store-guide)

- [Snapcraft Guide](https://www.electronjs.org/docs/tutorial/snapcraft-guide)

- [Application Packaging](https://www.electronjs.org/docs/tutorial/application-packaging)

- [Updates](https://www.electronjs.org/docs/tutorial/updates)

### Resources

- [Community Discussion](https://www.electronjs.org/community)

- [Community Showcase](https://www.electronjs.org/showcase)

- [Awesome Electron](https://www.electronjs.org/community#awesome-electron)

- [Electron Fiddle](https://www.electronjs.org/fiddle)

- [Electron API Demos](https://www.electronjs.org/api-demos)

- [Electron Forge](https://www.electronjs.org/forge)

- [Electron Builder](https://www.electronjs.org/builder)

- [Electron React Boilerplate](https://www.electronjs.org/react-boilerplate)

- [Electron Vue Boilerplate](https://www.electronjs.org/vue-boilerplate)

- [Electron Typescript Boilerplate](https://www.electronjs.org/typescript-boilerplate)

- [Electron Packager](https://www.electronjs.org/packager)

### Related Projects

- [Electron](https://www.electronjs.org/)

- [Electron Forge](https://www.electronjs.org/forge)

- [Electron Builder](https://www.electronjs.org/builder)

- [Electron Packager](https://www.electronjs.org/packager)

- [Electron Fiddle](https://www.electronjs.org/fiddle)

- [Electron API Demos](https://www.electronjs.org/api-demos)

- [Electron React Boilerplate](https://www.electronjs.org/react-boilerplate)

- [Electron Vue Boilerplate](https://www.electronjs.org/vue-boilerplate)

- [Electron Typescript Boilerplate](https://www.electronjs.org/typescript-boilerplate)

- [Electron React Typescript Boilerplate](https://www.electronjs.org/react-typescript-boilerplate)

- [Electron Vue Typescript Boilerplate](https://www.electronjs.org/vue-typescript-boilerplate)

- [Electron React Quick Start](https://www.electronjs.org/react-quick-start)

- [Electron Vue Quick Start](https://www.electronjs.org/vue-quick-start)

- [Electron Typescript Quick Start](https://www.electronjs.org/typescript-quick-start)

- [Electron React Typescript Quick Start](https://www.electronjs.org/react-typescript-quick-start)

- [Electron Vue Typescript Quick Start](https://www.electronjs.org/vue-typescript-quick-start)

BULDING FIRST APP WITH ELECTRON

Initializing your npm project

First, create a new directory for your project and initialize it as an npm project:

```bash
mkdir my-electron-app && cd my-electron-app
```

```bash
npm init
```

This will create a package.json file for your project. You can optionally skip this step by running npm init -y instead.

Installing Electron

Next, install Electron as a development dependency:

```bash
npm install --save-dev electron
```

Running your app

After installing Electron, you can now run it from your project's root folder:

```bash
./node_modules/.bin/electron
```

Alternatively, you can add a "start" script to your package.json file to make this easier:

```json
{
  "name": "my-electron-app",
  "version": "0.1.0",
  "main": "main.js",
  "scripts": {
    "start": "electron ."
  },
  "devDependencies": {
    "electron": "^1.6.2"
  }
}
```

Then, you can simply run npm start to start your app.

```bash
npm start
```

Creating your first window

Now that you have a basic Electron app running, let's create your first browser window. To do so, add the following lines to your main.js file:

```js
const { app, BrowserWindow } = require("electron");

function createWindow() {
  // Create the browser window.
  let win = new BrowserWindow({ width: 800, height: 600 });

  // and load the index.html of the app.
  win.loadFile("index.html");

  // Open the DevTools.
  win.webContents.openDevTools();
}

app.on("ready", createWindow);

// Quit when all windows are closed.

app.on("window-all-closed", () => {
  // On macOS it is common for applications and their menu bar

  // to stay active until the user quits explicitly with Cmd + Q

  if (process.platform !== "darwin") {
    app.quit();
  }
});

app.on("activate", () => {
  // On macOS it's common to re-create a window in the app when the

  // dock icon is clicked and there are no other windows open.

  if (win === null) {
    createWindow();
  }
});
```

This code creates a new BrowserWindow instance and loads index.html into it. You can learn more about Electron's main process and the BrowserWindow module in the docs.

Creating an index.html file

Next, create an index.html file in the root folder of your project:

```html
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8" />

    <!-- https://electronjs.org/docs/tutorial/security -->

    <meta
      http-equiv="Content-Security-Policy"
      content="script-src 'self' 'unsafe-inline';"
    />

    <title>Hello World!</title>
  </head>

  <body>
    <h1>Hello World!</h1>

    We are using node
    <script>
      document.write(process.versions.node);
    </script>
    , Chrome
    <script>
      document.write(process.versions.chrome);
    </script>
    , and Electron
    <script>
      document.write(process.versions.electron);
    </script>
    .
  </body>
</html>
```
