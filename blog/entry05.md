# Entry 5
##### 4/27/25

During these last few weeks on working toward the MVP (Minimum Viable Product), me and my group decided to finalize our project and make sure the player has something to do within the game. Our group delicated different tasks to different group members so we could try our best to avoid any merge conflicts when we commit and can work on the project at the same time. We needed to add a resource menu so I learnt how to use the Godot control nodes as well as how to manage the resources in the file system. My partner Benjamin started with the basic layout of what resources we wanted but I finished it by making it increase by a set interval. 

Me and Zi Xuan Yu also worked together in a discord call to figure out how to detect a tree nearby when placing a building. This part was extremely dificult because of the complication that the tile "coordinates" were different than the godot "coordinates". The value of the tile coordinates would be the number of tiles while the godot coordinates counted by pixels. 

In the end, we figured out a function that would convert the pixel coordinates to the tile coordinates. By making the pixel coordinates position relative to the position of the tile, it checks the position of both and how they relate to eachother. This uses `local_to_map` so it can convert the coordinates of the local workpace to the tilemap coordinate. 

```gdscript
func get_building_position(pos: Vector2):
	return $"../../TileMapLayer".local_to_map(
		$"../../TileMapLayer".to_local(
			pos))
```
[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
