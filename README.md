# electron-npm-install

An API (and command-line tool) to execute `npm install` inside of electron projects, configured properly to build native dependencies with the right versions of V8 and Node to work in Electron.

## Installation

```
npm install --save electron-npm-install
```
    
## Usage

```js
var install = require('electron-npm-install');
    
install(["foo", "bar"], function(err) {
  if (err) {
    console.log('Installation failed.');
  } else {
    console.log('Installation succeeded!'); 
  }       
});
```
    
## API

### install(pkgs, done)

Run `npm install` where:

- `pkgs` is an array of packages to install - optional
- `done` is a function called when the command has finished - optional 
