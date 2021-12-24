# Yet Another Ground Station GUI
## What is this?
This is a reimplimenation of the Purdue Orbital Ground Station Graphical User Interface as an electorn app to allow for better installation, compatability and styling. This is the window that the flight team will use to communicate with the Ground Station and ultimately the Launch Structure by sending commands and receiving data. It was bootstrapped with [Create React App](https://github.com/facebook/create-react-app) and served with [Electron](https://www.electronjs.org/).

## Sounds cool, how do I get set up for development?
The first thing you're going to want to do is clone this repository:
```sh
git clone https://github.com/purdue-orbital/yags-gui.git
```

From there, simply install all necessary dependencies using the node package manager:
```sh
npm install
```
Congratulations you are now ready to begin development on the front-end!!

## So what can this repo do?
A list of available `npm` scripts with small descriptions has been provided bellow to answer that very question!

### `npm start`
Sets up a development server on [https://localhost:3000](https://localhost:3000). This page will reload if edits are made and show linting errors that may be present. Generally just a nice way make changes and develop the front-end.

### `npm run test`
Launches the test runner in the interactive watch mode.

### `npm run build`
Builds the react app for production in the `build/` folder and prepares it for deployment.

### `npm run eject`
**Note: this is a one-way operation. Once you `eject`, you can’t go back!**\
This command will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. It is very unlikely you'll ever need to do this, but option is here should you deem it necessary (but make sure you have a good reason).

### `npm run electron`
Creates an electron window listening on [https://localhost:3000](https://localhost:3000). This window is exactly what it will look like for people using the ground station in the field, so it makes most since to develop using this window rather than any old browser.

### `npm run ele`
An alias for `npm run electron`. Do you seriously expect me to type out *electron* every time? Like holy cow its 8 letters, you must be mad.

### `npm run dev`
Fully runs the app in development mode. Runs both `npm start` and `npm run electron` concurrently, and should either process end, the other is also forcefully quit. Useful for showing demonstrations without continually building and re-installing the app or running both commands separately.

### `npm run package`
This command will build the react app for distribution and will use `Electron Forge` to package the electron application into a platform specific format and put the result in an `out/` folder. Please note that this does not make a distributable format!! To make proper distributables, use the `npm run make` script.

### `npm run make`
This will fully make the app as a distributiable. The type of distributable is dependenent on the os and archetecure of your current machine. Currently it is able to build to an x64 `.deb` and `.rpm`. 

### `npm run clean`
Simply removes the `build/` and `out/` folders.

