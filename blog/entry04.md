# Entry 4
##### 3/16/25

Nearing our due date of our Minimum Viable Product (MVP), my group decided that we needed to start "creating a prototype" of our project in the engineering design process. I first made a tilemap of 40x40 for my map and added a layer of trees. 

Using [this tutorial](https://www.youtube.com/watch?v=GiZuWjXmvcc), I created added collisions to my tilemap on the borders. This way, my character would not be able to leave the map. I also added collisions to the trees but this was a struggle because it worked slightly differently to the other collision polygon that godot uses. Instead, I needed to select the tiles and place a collision map on top of each specific tile. This way, I don't need to place a tile collision for every individual tile. It was very difficult to get this correct because I also noticed that my character would walk on top of the trees instead of around it. To fix this, I realised I needed to seperate the tilemap layer of the leaves and the trunk. I tried many differen things but such as changing the y layer but the thing that worked for me was changing the z-layer. This z-layer determined how front or back the layer was from the top and I placed my leaves at the very top so the player can go behind the leaves and behind the trees. It was weird to change the layering because I had to keep track of all the layers I put for each. In the end, the floor layer was layer 0, the trunks were layer 1, the player was layer 3 and the leaves were layer 4. This made it so the player would walk around the trees and it successfully added the collisions. 

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
