# Python Impact Web Server

A simple self contained web server for ImpactJS that allows you to run both the game and weltmeister (level editor) without the need for Apache.


## How do I use this?

Just drop server.py in your impact folder along with your index.html file.

Then in terminal simply run:

	python server.py

Visit http://localhost:8080 for the game or http://localhost:8080/editor for the weltmeister level editor.


## Why did you build this and why is it useful?

I have a strange aversion to anything PHP and trying to develop with multiple ImpactJS games becomes a serious pain in the ass with Apache.

With this server all you need to do is change the settings port and you could even run many servers simultaneously.

Oh and technically I didn't build it, I forced a super talented friend of mine [Armon](http://github.com/armon) to hack this together for me.


## Caveats

**This should be used as a development tool only**

Don't use this to serve your live game, it's likely to have many issues and is no way designed to scale or even provide proper asset caching.


## Configuration Settings

At the top of server.py is a `SETTINGS` dictionary that provides a couple tweakable settings.

### Port

Used to specify the server port. This shouldn't need changing unless you are running multiple instances of server.py at the same time.

### Logging

Defaults to False, if set to True, you will see http request logs in terminal.

### API-*

This allows you to configure the API endpoints hit by weltmeister. Only change these if you changed them in the weltmeister config.js file.

If you have no idea what I am talking about don't touch them.

### Image-Types

Don't touch this unless you know what you are doing. It determines what images can be displayed and used in Weltmeister.

### MimeTypes

This is a dictionary used to add your own custom mime-types. You only need to use this if you are noticing certain file types not being served properly.

## Command Line Options

The following options may be used:

* -p <port> or --port=<port>  : Port to run server on
* -l or --log  : Enable Logging
* -b or --browser  : Opens default browser with 2 tabs for the editor and game
* -f or --firefox  : Opens Firefox with 2 tabs for the editor and game
* -s or --safari  : Opens Safari with 2 tabs for the editor and game

## Contributers

This project wouldn't be possible without the awesome contributions of a few key people

* [Armon Dadgar](https://github.com/armon)
* [Lea Anthony](https://github.com/lea-anthony)

## License

This project is under the [MIT License](http://en.wikipedia.org/wiki/MIT_License)
