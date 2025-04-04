# Tool Learning Log

## Tool: Unity, Changed to Godot

## Project: **X**

---

### 10/14/24:
* I was unable to start Unity for now so instead I started to read the Documentation
* Game View VS Scene view
  Game view shows how the game looks through the player
  
  Scene view allows you to navigate through the scene of the game (such as a 3D/2D rendering of the background)

There are a lot of graphics that Unity has built in that lets you get started easier
Scripting allows the players to input commands and lets the game do something
* We can choose our own code editor (our workspace) when working with scripts

### 10/20/24:
I downloaded unity and tried some basic tools
Using a tutorial, I learned the UI of the app and what it contains
* The project pannel contains what is going to be in the project
* scene is what you see
* hierachy lists all the object in the current level
* inspector allows you to change those objects
Following the tutorial, I tried adding physics and adding a component to a cube (gravity)

### 10/27/24

using videos from this site: https://kidscancode.org/godot_recipes/4.x/g101/start/index.html

* node is an object that can represent some kind of specialized game function
* nodes are the "objects" or maybe classes
* created a sprite2D node and inspected it to see its properties
* sprite2D is an object of multiple other classes, each time adding on a new property
* you can put a node inside another node and it will become its "children" - if you move the adult, the child will also move
* you can attach a script to a node and use it to control the node

### 11/17/24

Using https://www.youtube.com/watch?v=ZutpG0_CYrQ, I played around with a tile map and its properties

* I strugged to download the files onto my tilemap but eventually got it to work
* I need to create a tile set after create a TileMap node into the scene. 
* then I drag the files onto the scene
* this allows me to directly add the tiles onto my file map
* right click allows me to delete
* to place an object over another, I need to add layers

### 11/24/24

* I created a bigger scene and I used the newer layers tile map
* I created boundaries of the properties in case for movement
* I thought about my own tilemap to use
* tried to figure out how to create some movement using the tile map
* however, i could not figure out or find the right tutorial

### 12/1/24

* made an interactive tilemap that changes if they are a certain tile using https://www.youtube.com/watch?v=O4AQtCWNQmo
* tried to create a node that interacts when clicked
* using the documentation and the script, I managed to make the icon display sometimes in the output when it is clicked
* however, i want to make a tile interactive and need to test how to make a tile work the same way

### 1/5/25

* as a group, we decided to connect our projects on godot with github so we can collaborate
* I created some sprite of buildings and the character so we could get started on our project

### 3/3/25

* created a 3d tile for the character model
* created a 2d tile for the common house
* imported the two images to godot
* Attempted to create a tileset for these images but it didn't work, it seems i would need more tiles for a proper tile set
* next time, i will create a full tile set or use a template so I can add collision for my character model and make a tile map

### 3/10/25

* used a tileset from online as a temperary tilemap
* create a tilemap
* changed the default character model with my own model
* tested the collisions of the map
* next time, I will change adjust the nodes that we have to make sure they line up and work properly with eachother
* rewatched older videos from before to refresh my memory

### 3/23/25

* added trees for more scenery by importing another design
* I tried to fix a visualization error by removing the background on one of the tiles but it did not work as when I looked it up, the tools needed required money
* Used https://www.youtube.com/watch?v=GiZuWjXmvcc to add collisions on both the border and the trees
* I used the collision polygon 2d to create the border for the outside and created a condition to where if the player was in front of the tree, it would go in front and if the player was behind the tree, the player would be behind

### 3/31

* I added the buildings from my 2d Models
* I tried to create a shop using this tutorial [https://www.youtube.com/watch?v=-IdFbcKro2c&list=PLylNHWOqRhsHLNvcthzeOjkAHzveDtgLk&index=2](https://www.youtube.com/watch?v=-IdFbcKro2c&list=PLylNHWOqRhsHLNvcthzeOjkAHzveDtgLk&index=2)
* I had to update my partner's currently menu that he worked on because it was small and very little detail
* I added the building from the model into the stop
* I struggled on learning the godot script because it was my first time using it and the file system was confusing as I didn't understand whether or not the user had it or not
<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
