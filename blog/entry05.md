# Entry 5
##### 4/27/25

During these last few weeks on working toward the MVP (Minimum Viable Product), me and my group decided to finalize our project and make sure the player has something to do within the game. Our group delicated different tasks to different group members so we could try our best to avoid any merge conflicts when we commit and can work on the project at the same time. We needed to add a resource menu so I learnt how to use the Godot control nodes as well as how to manage the resources in the file system. My partner Benjamin started with the basic layout of what resources we wanted but I finished it by making it increase by a set interval. I partly used [This Video](https://www.youtube.com/watch?v=h5vpjCDNa-w) to help me with setting up the basic resources. It also helped me think about how the resources were saved onto godot. Here are some examples of some methods on how the resources (wood and population) increases.

```gdscript
func produce_resources():
	for res in production_rates:
		resources[res] += production_rates[res]
		
func add_production(resource_name: String, amount: int):
	if production_rates.has(resource_name):
		production_rates[resource_name] += amount
	else:
		production_rates[resource_name] = amount
```

I also created the menu or display for which the player would see the amount of wood, people, etc. Using [This video](https://www.youtube.com/watch?v=5Hog6a0EYa0), it thought me how to use control nodes. It taught me that these control nodes are the best the displaying something (which was our goal) and the different parts that it can have. For each resource we wanted, we would have a panel, a container and a label. The panel would be the rectangle display, the container would be the logo and the label would go back to the resources and take that number to display. Then, I realised that it wasn't showing correctly and would become very small, especially when we got our contruction screen. To fix this, I added a canvas layer. This canvas layer made it so it would be fixed to the screen and would not change no matter what. 

Me and Zi Xuan Yu also worked together in a voice call to figure out how to detect a tree nearby when placing a building. This part was extremely dificult because of the complication that the tile "coordinates" were different than the godot "coordinates". The value of the tile coordinates would be the number of tiles while the godot coordinates counted by pixels. In the end, we figured out a function that would convert the pixel coordinates to the tile coordinates. By making the pixel coordinates position relative to the position of the tile, it checks the position of both and how they relate to eachother. This uses `local_to_map` so it can convert the coordinates of the local workpace to the tilemap coordinate. 

```gdscript
func get_building_position(pos: Vector2):
	return $"../../TileMapLayer".local_to_map(
		$"../../TileMapLayer".to_local(
			pos))
```
At every location where we needed to use this coordinate, we would call this function. However, there were specific places that we needed to place to function because there were parts of our code that were based on the map coordinate. If we wanted to use this function correct, we need to use it only when dealing with the tilemap and nothing else. 

In the end, we ended up with our MVP that included a contruction button to build a house or a lumberyard, resources menu, a collision map and ways to manipulate the resources within our lumberyard menu. Together, we talked a lot during our spring break to finish this project and certainly developed great communication. We talked a lot about how our project was going to work and our priorities. We debated on how our resources was going to work like how the player would gain them and use them and also our priorities. There were a couple things on our MVP that did not finish but the time was used on another task that was more important. I certainly developed embracing failure because the amount of errors I would get when running to get the tiles was a lot. There were times where the contruction menu became too slow because we changed the tile coordinates and there were also times where placing near a tree would completely crash. However, I understood that in order to complete this project, I needed to figure out what these mistakes were by printing and work my way out. 
[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
