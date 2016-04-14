[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

# React Tutorial

This is the React comment box example from [the React tutorial](http://facebook.github.io/react/docs/tutorial.html).

## To use

(Note: I've modified the initial NodeJS configuration to use the NodeJS `nodemon` module for server-side hot-loading. i.e server-side scripts are reloaded automatically without the need to restarting server.````)

```.sh
npm install
npm run nodemon-debug
```

And visit <http://localhost:3000/>. Try opening multiple tabs!

## Changing the port

You can change the port number by setting the `$PORT` environment variable before invoking any of the scripts above, e.g.,

```sh
PORT=3001 nodemon --debug server.js
```

# A not on comments.json file

The file `comments.json` is a "fake" database (a JSON file) that changes from time to time - depending on user interaction with the web application.

Though this file was initially tracked via Git, I've run the following commands to assume this file is unchanged - so this file will stop being flagged by git ever time new data is added / deleted.

```.sh
git update-index --assume-unchanged comments.json
```

To undo this (i.e. if you really wish to start tracking this file which is not advisable) you can do this:

```.sh
git update-index --no-assume-unchanged comments.json
```
