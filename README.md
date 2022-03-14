# JmvGenerator

Plugin to generate terrain for Minecraft Java with nukkit.  
This is not a product of Minecraft, nor is it endorsed or associated with Mojang.

## Be careful
1. It may not work depending on the environment. Please be sure to try a sample before purchasing.  
In my case, it worked on my desktop PC and rental vps server, but not on my laptop.
2. This plugin does not include commands for generating worlds.
3. This plugin is loaded in a special way that may cause other plugins to stop working.

## How to install
1. Download the Minecraft 1.16.5 server.  
https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar

2. Unzip the downloaded zip file and arrange the files like a tree.
```
├── plugins/
│   └── JmvGeneratorPlugin.jar
├── nukkit.jar
├── JmvLoader.jar
├── minecraft.jar
└── JmvLib.jar
```

3. Execute command.
```
java -jar JmvLoader.jar -library JmvLib.jar
```

4. Agree with eula.  
Agree as eula.txt is generated.

5. Execute the command again.

## JmvLoader argment
|name|description|
|:-----------|:-----------|
|nukkit|Specify the path of nukkit.jar|
|minecraft|Specify the path of minecraft.jar|
|library|Specify the path of JmvLib.jar|
```
java -jar JmvLoader.jar -nukkit nukkit-1.0-SNAPSHOT.jar -minecraft server.jar -library JmvLib.jar
```

## Generator name
- jmv_overworld
- jmv_nether
- jmv_end
- jmv_large_biomes
- jmv_amplified
- jmv_single_biome (use biome option)
- jmv_caves (use biome option)
- jmv_floating_is_land (use biome option)

## Biome option
Fill in the presets to specify the biome.  
The biome that can be used is the Java version of the biome name.
<details>
 <summary>
  List of biome
 </summary>  
 <ul>
  <li>ocean
  <li>plains
  <li>desert
  <li>mountains
  <li>forest
  <li>taiga
  <li>swamp
  <li>river
  <li>nether_wastes
  <li>the_end
  <li>frozen_ocean
  <li>frozen_river
  <li>snowy_tundra
  <li>snowy_mountains
  <li>mushroom_fields
  <li>mushroom_field_shore
  <li>beach
  <li>desert_hills
  <li>wooded_hills
  <li>taiga_hills
  <li>mountain_edge
  <li>jungle
  <li>jungle_hills
  <li>jungle_edge
  <li>deep_ocean
  <li>stone_shore
  <li>snowy_beach
  <li>birch_forest
  <li>birch_forest_hills
  <li>dark_forest
  <li>snowy_taiga
  <li>snowy_taiga_hills
  <li>giant_tree_taiga
  <li>giant_tree_taiga_hills
  <li>wooded_mountains
  <li>savanna
  <li>savanna_plateau
  <li>badlands
  <li>wooded_badlands_plateau
  <li>badlands_plateau
  <li>warm_ocean
  <li>lukewarm_ocean
  <li>cold_ocean
  <li>deep_warm_ocean
  <li>deep_lukewarm_ocean
  <li>deep_cold_ocean
  <li>deep_frozen_ocean
  <li>legacy_frozen_ocean
  <li>bamboo_jungle
  <li>bamboo_jungle_hills
  <li>sunflower_plains
  <li>desert_lakes
  <li>gravelly_mountains
  <li>flower_forest
  <li>taiga_mountains
  <li>swamp_hills
  <li>ice_spikes
  <li>modified_jungle
  <li>modified_jungle_edge
  <li>tall_birch_forest
  <li>tall_birch_hills
  <li>dark_forest_hills
  <li>snowy_taiga_mountains
  <li>giant_spruce_taiga
  <li>giant_spruce_taiga_hills
  <li>modified_gravelly_mountains
  <li>shattered_savanna
  <li>shattered_savanna_plateau
  <li>eroded_badlands
  <li>modified_wooded_badlands_plateau
  <li>modified_badlands_plateau
  <li>soul_sand_valley
  <li>crimson_forest
  <li>warped_forest
  <li>basalt_deltas
  <li>small_end_islands
  <li>end_midlands
  <li>end_highlands
  <li>end_barrens
  <li>the_void
 </ul>
</details>

#### Example
```
worlds:
 sample_world:
  seed: 100
  generator: jmv_single_biome:biome=desert
```
