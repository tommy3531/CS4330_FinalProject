# Comparing C++ to Swift 3

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

Swift 3 is a new Open Source language that was created by Apple in 2002.

  - Language Purpose
  - Unique features
  - Name spaces
  - Types
  - Classes
  - Instance references
  - Properties
  - Interface / Protocl
  - Inheritance / extensions
  - Reflection
  - Memory management
  - Comparisons of references and values
  - NUll/nil references
  - Errors and execption handling
  - lambda expressions, closures or functions as types
  - Implementation of listeners and event handlers
  - Singleton
  - Procdural Programming
  - Functional Programming
  - Multithreading

# Language Purpose
Swift 3: Explain the language and why it was created
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
# Unique features
Explain the unique features: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
# Name spaces
1. How are name spaces implemented?
    - To access items in one namespace from another we must first import the module             using the import declaration.   The import delcaration consists of the import           keyword followed by the module name.  
        ```
        import moduleName
        ```
2. How are names spaces used?
    - A namespace acts as a border/boundary and another namespace can not access               another namespace  without mentioning it first.  Name spaces provides a virtual         partition seperating the names in one namespace from names in another.  By              creating this seperation two items can be declared with the same name                   as long as they are in different namespaces.  In Swift namespaces are used as a         boundary when a import declaration is used within a .swift file.  For example,          if I was using Alamofire to make rest calls to an API, I would import the               module, which gives the current file access to Alamofire.  

        ```
        import Alamofire
        ```
        
        The import declaration can be used to make a sepecific classe or method                 available to the current namespace. 
        
        ```
        import UIKit.NSData
        ```

Explain how Name spaces work: 
```
This is used to write an example
cd dillinger
npm install -d
node app
```
### Types
Explain Types: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Classes
Explain Classes: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Instance references
Explain Instance References: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Properties
Explain Properties: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Interface / Protoclo
Explain Protocols: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Inheritance / extensions
Explain Inheritance:
Explain extensions:

```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Reflection
Explain Reflection:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Memory management
Explore Memory management: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Comparisons of references and values
Explain references and values: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### NUll/nil references
Explain NULL references: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Errors and execption handling
Explain Errors: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### lambda expressions, closures or functions as types
Explain Lambda:
Explain closures: 
Explain functions are types: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Implementation of listeners and event handlers
Explain listeners:
Explain event handlers:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Singleton
Explain singleton:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Procdural Programming
Explain Procedural Programming: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Functional Programming
Explain functional Programming:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Multithreading
Explain Multithreading: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```





Dillinger uses a number of open source projects to work properly:

* [AngularJS] - HTML enhanced for web apps!
* [Ace Editor] - awesome web-based text editor
* [markdown-it] - Markdown parser done right. Fast and easy to extend.
* [Twitter Bootstrap] - great UI boilerplate for modern web apps
* [node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework [@tjholowaychuk]
* [Gulp] - the streaming build system
* [Breakdance](http://breakdance.io) - HTML to Markdown converter
* [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

### Installation

Dillinger requires [Node.js](https://nodejs.org/) v4+ to run.

Install the dependencies and devDependencies and start the server.



For production environments...

```sh
$ npm install --production
$ npm run predeploy
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md] [PlDb] |
| Github | [plugins/github/README.md] [PlGh] |
| Google Drive | [plugins/googledrive/README.md] [PlGd] |
| OneDrive | [plugins/onedrive/README.md] [PlOd] |
| Medium | [plugins/medium/README.md] [PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md] [PlGa] |


### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantanously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma test
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 80, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version}
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 80 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Todos

 - Write MOAR Tests
 - Add Night Mode

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
