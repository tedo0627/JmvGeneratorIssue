# JmvGenerator
nukkitでjava版のMinecraftと同じ地形を生成するプラグイン  
これはMinecraftの製品ではなく、またMojangによって承認または関係付けられていません

BOOTH: https://tedo0627.booth.pm/items/3719253

## 注意
1. このプラグインは環境によって動かない場合があります。まずサンプルを試してから購入してください。  
私の場合、デスクトップPCとvpsサーバーでは動きましたが、ノートPCでは動きませんでした。
2. このプラグインはワールドを作成するコマンドが含まれていません。
3. このプラグインは特殊な方法で読み込ませているため、他のプラグインが動作しない場合もあります。

## 製品版とサンプル版の違い
1. 対応しているジェネレーターがオーバーワールドのみ
2. 生成される範囲が16×16チャンクのみ
3. 建物が生成されない

## 導入方法
1. マイクラ1.16.5のサーバーをダウンロードする
https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar

2. ダウンロードしたzipファイルを解凍して、ファイルをツリーのように配置する
```
├── plugins/
│   └── JmvGeneratorPlugin.jar
├── nukkit.jar
├── JmvLoader.jar
├── minecraft.jar
└── JmvLib.jar
```
3. コマンドを実行する  
```
java -jar JmvLoader.jar -library JmvLib.jar
```
4. eulaに同意する  
eula.txtが生成されるので、同意する

5. 再度コマンドを実行する

## JmvLoaderのオプション
|name|description|
|:-----------|:-----------|
|nukkit|nukkit.jarのパスを指定する|
|minecraft|minecraft.jarのパスを指定する|
|library|JmvLib.jarのパスを指定する|
```
java -jar JmvLoader.jar -nukkit nukkit-1.0-SNAPSHOT.jar -minecraft server.jar -library JmvLib.jar
```

## 対応しているジェネレーター名
- jmv_overworld
- jmv_nether
- jmv_end
- jmv_large_biomes
- jmv_amplified
- jmv_single_biome (バイオームを選択する)
- jmv_caves (バイオームを選択する)
- jmv_floating_is_land (バイオームを選択する)

## バイオームの選び方
presetでバイオームを指定する  
使えるバイオームの名前はjava版のMinecraftのバイオームの名前
<details>
 <summary>
  使えるバイオーム一覧
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

#### 例
```
worlds:
 sample_world:
  seed: 100
  generator: jmv_single_biome:biome=desert
```
