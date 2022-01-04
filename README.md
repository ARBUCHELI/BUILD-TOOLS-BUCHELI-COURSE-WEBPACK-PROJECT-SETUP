# BUILD-TOOLS-BUCHELI-COURSE-WEBPACK-PROJECT-SETUP

## In order to set up webpack in a project, follow the next steps:

* npm init -y (Webpack is a Node package. To use Node packages, we need a package.json which holds important project metadata about any Node project. We can initialize a Node
project using npm init in the terminal to make a package.json file. We can use the -y flag to use the default values for the metadata fields).

* npm install --save-dev webpack webpack-cli (We need two packages, webpack and webpack-cli, to build our Webpack project with the command line. webpack contains the main
functionality, but webpack-cli allows command-line access to Webpack. We want these tools to be developer dependencies because they will not be used when the final product is
running. We use npm install and the --save-dev flag to save packages as developer dependencies).

* A Webpack project requires an entry point where it will find the main file to bundle. Webpack will throw a long error indicating a problem with main if there are no files at
the entry point. The default Webpack entry point is index.js in a src folder, although this can be changed. If we want to use the default entry point, we should make an src folder
with an index.js inside of it.

* A build command is often defined in the scripts section of package.json for running Webpack. You can find more information on the scripts section here. Using a build command
makes the way we build the project independent of what build tools we use. We define the build command like so:A build command is often defined in the scripts section of 
package.json for running Webpack. You can find more information on the scripts section here. Using a build command makes the way we build the project independent of what build 
tools we use. We define the build command like so:
```
"scripts": {
  "build": "webpack --watch",
},
```

* npm run build
