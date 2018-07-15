# Changes / Requirements

Install this in a folder with a path that has no spaces... breaks nodemon.

## Install MongoDB

Need to install MongoDB: See https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/

Open cmd as admin

Download Community Edition installer from [here](https://www.mongodb.com/download-center?_ga=2.228222740.822904951.1531591132-1876779726.1531591132&_gac=1.56154201.1531591132.Cj0KCQjwvqbaBRCOARIsAD9s1XCHlpMXONovPaxv2i31VJNtFhJ8D91Wp-dicRY-xIo_PFPld8j3TWMaApR8EALw_wcB#community).

Installed MongoDB as a network service, plus MonngoDB Compass (UI for dbs)

## Code setup

Quickstart at http://mern.io/documentation.html

```
npm i -g npm@latest

git clone https://github.com/Hashnode/mern-starter.git
cd mern-starter
git checkout -b dev
npm install
```

Getting install issues about Python. See https://stackoverflow.com/questions/15126050/running-python-on-windows-for-node-js-dependencies

There's an issue where node-gyp relies on 8.1 windows compiler, but you have Win10:
https://medium.com/@TaylorAckley/run-into-a-node-gyp-compilation-error-on-windows-10-heres-what-to-do-ef5fe6c4081

Open VS 2015, New project -> C++, Visual C++ -> Windows, Install Windows 8.1 and Windows Phone 8.0/8.1 Tools -> OK, Install -> Next, Update

Open cmd as admin:

```
npm install --global --production windows-build-tools
npm install --global node-gyp
setx PYTHON "%USERPROFILE%\.windows-build-tools\python27\python.exe"
```
Restart cmd as admin:

`set PYTHON` (returns path to Python successfully)

`npm install` (have to run this from in cmd as admin, not from terminal in VS Code)

Got some security warnings. `npm audit` to list. Installed all recommended fixes (except last one, waiting on dev to update). 

`npm start`, running at localhost:8000