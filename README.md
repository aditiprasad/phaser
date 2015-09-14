# Phaser
> Phaser is an HTML5 game-development framework for both mobile and desktop games. It is heavily based on flixel. It uses Pixi.js for WebGL and Canvas. It's free under MIT thing.

## Download Phaser
There are a number of ways to download Phaser.
### Github :
You can clone the git repository via https, [ssh](https://github.com/photonstorm/phaser) or with the Github Windows or Mac clients.

### npm :
Install via npm
```
npm install phaser
```

### CDN :
Include the following in your html :
```
<script src="//cdn.jsdelivr.net/phaser/2.4.3/phaser.js"></script>

```

or the minified version :
```
<script src="https://cdnjs.cloudflare.com/ajax/libs/phaser/2.4.3/phaser.js"></script>
```

## Making our game

We first create a game object to run all the methods through. We do this like so:
```
var game = Phaser.Game(width, height, thirdParam, DOM_ID, {preload: preload, create: create, update: update, render: render});
```
```game``` is the object. Below are the details of the arguments:

```width``` is the width of the game window (world).
You can figure out what ```height``` is on your own.

```thirdParam``` renders what context you want to use. There are 3 arguments that you can use: Phaser.CANVAS, Phaser.WEBGL, or Phaser.AUTO. You should pretty much always use Phaser.AUTO

```DOM_ID``` is the ID of the DOM element that you want to attach the phaser window to. You can pass it an empty string ' ' to just append the window straight to the body.

The fifth parameter, is an object containing the references to the essential phaser functions; preload, create, update, and render. As always, you can name the values of the key/value pair whatever you want, but don't be an weirdo, just name the values preload create update and render. KISS.


Now we must define the essential functions. Below the instantiation of your game object, just define the functions using the names that you gave the values in the fifth argument of your game object.

```
function preload(){

}
function create(){

}
etc.
```

Inside the ```preload``` function is where you put all your data, like images, etc.

```create``` is where you load up that data/images to paint them in the window.

```update``` is where you update that data that you created in create(). (lol). But srsly this is where you add movement logic and all that stuff etc.

```render``` seems to be for debugging.

#### [Phaser Docs](http://phaser.io/docs) 
