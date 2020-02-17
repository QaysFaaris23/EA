# MY COMMITMENTS TO THE SCDF TRACKED VEHICLE
Basically as the head mechanical designer i am tasked to do everything about the chassis and moving parts. To begin, i first designed the main platform to mount the turret and the engine compartment.I split this platform into two, engine platform to hold the "engine compartment" which houses the electronics and turret platform to hold the turret. I ensures that they are in seperate compartments so that any water leakage from the nozzle on the turret wont spill into the electronics compartment. See the photo below

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform1.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform2.PNG" width ="300">

I used a partial V shaped slider to secure both platforms into one rigid object, and secured them to the chassis of the tank with M10 screw and nut

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform5.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform6.PNG" width ="300">

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform4.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/MainPlatform3.PNG" width ="300">

Next i move on the "engine compartment". I designed rather large compartment to easily store the electronics component, which is easily accesible with a sliding lid on top. See the photos below

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment1.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment2.PNG" width ="300">

Much like the engine platform, i also used a V shaped slider to secure my engine compartment and the platform, and with an additional 5.8 diameter bolt and nut to further secure it to ensure its rigidity

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment3.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineComaprtment4.PNG" width ="300">

As for the lid its tight fit

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/EngineCompartment5.PNG" width ="300">

Next ill shall move on to the turret. A servo rest inside the turret platform, and the turret ring is secured to the servo with a screw which holds the turret ring between the head of the screw and the servo. Do note theres a thread inside the servo head which can be screwed into

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret1.PNG" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret2.PNG" width ="300">

Next the z axis servo holder is placed into one of the turret ring's pin slot. I added a small out facing pillar so that the servo holder does not fall right through the pin slot

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret3.PNG" width ="300"><img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret4.PNG" width ="300">

Next i we insert the servo, followed by the modular mount and screw to secure them together

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret5.PNG" width ="300">https://github.com/QaysFaaris23/ScdfVehicle/blob/master/FaarisJOurnals/Turret6.PNG
# New Features!

  - Import a HTML file and watch it magically convert to Markdown
  - Drag and drop images (requires your Dropbox account be linked)


You can also:
  - Import and save files from GitHub, Dropbox, Google Drive and One Drive
  - Drag and drop markdown and HTML files into Dillinger
  - Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.

### Tech

Dillinger uses a number of open source projects to work properly:

* [AngularJS] - HTML enhanced for web apps!
* [Ace Editor] - awesome web-based text editor
* [markdown-it] - Markdown parser done right. Fast and easy to extend.
* [Twitter Bootstrap] - great UI boilerplate for modern web apps
* [node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework [@tjholowaychuk]
* [Gulp] - the streaming build system
* [Breakdance](https://breakdance.github.io/breakdance/) - HTML to Markdown converter
* [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

### Installation

Dillinger requires [Node.js](https://nodejs.org/) v4+ to run.

Install the dependencies and devDependencies and start the server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

For production environments...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

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

By default, the Docker will expose port 8080, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

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

 - Write MORE Tests
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