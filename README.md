# grunt-services

> Start and Stop database services

## Getting Started
This plugin requires Grunt.

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-services --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-services');
```

## The Tasks

All tasks are plain tasks, which means you have to include them in `grunt.registerTask()` statements or call them directly from command line. The available tasks are:

* **startRedis** Start Redis database.
* **startMongo** Start Mongodb database.
* **startPostgres** Start Postgres database.
* **stopRedis** Stop Redis database.
* **stopMongo** Stop Mongodb database.
* **stopPostgres** Stop Postgres database.


### Sample Setup

Create `start` and `stop` aliases for starting and stoping the services:

```js

grunt.initConfig({ /* ... */ });

grunt.registerTask('start', 'Start all required services', ['startRedis', 'startMongo']);
grunt.registerTask('stop', 'Stop all services', ['stopRedis', 'stopMongo']);
```

## Release History

- **v0.1.0**, *16 Apr 2015*
    - Fixed redis shutdown, thank you [@itsjustcon](https://github.com/itsjustcon).
- **v0.0.3**, *21 Nov 2014*
    - Changed the way Mongo is shutdown, instead of a brutal kill we now use the suggested by mongodb way, thank you [@victorsand](https://github.com/victorsand).
- **v0.0.2**, *25 Apr 2014*
    - Fix for linux environments, thankyou [@bryanlester](https://github.com/bryanlester).
- **v0.0.1**, *15 Feb 2014*
    - Big Bang

## License

Copyright (c) 2014 Thanasis Polychronakis. Licensed under the MIT license.
