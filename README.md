# WorkAdventure Map Starter Kit

This is a starter kit to help you build your own map for [play.zkm.world](https://play.zkm.world).

# Edit the map

In order to build your own map, you need:

- the [Tiled editor](https://www.mapeditor.org/) software
- "tiles" (i.e. images) to create your map (this starter kit provides a good default tileset for offices)

## Loading the map in Tiled

The sample map is in the file `map.json`.
You can load this file in [Tiled](https://www.mapeditor.org/).

Now, it's up to you to edit the map and write your own map.

Some resources regarding Tiled:

- [Tiled documentation](https://doc.mapeditor.org/en/stable/manual/introduction/)
- [Tiled video tutorials](https://www.gamefromscratch.com/post/2015/10/14/Tiled-Map-Editor-Tutorial-Series.aspx)

## Create your own tiles

Tiles are PNG images divided in a 32x32 pixel grid. It is not possible to use other grid sizes (e.g. 16x16). Check out the example tile files in the `public/tiles/` folders.

# Deploy the map

The `.gitlab-ci.yml` file in this repository automatically deploay the contents of `public/` after each push. The URL can be found under Settings -> Pages.

If the repository belongs to the user `loelkes` and is named `awesome-map` the URL will be `loelkes.gitlab-pages.zkm.de/awesome-map/`

Open your map with `play.zkm.world/_/global/<link to the map.json>`, in this example `play.zkm.world/_/global/loelkes.gitlab-pages.zkm.de/awesome-map/map.json`.

# Behind the scenes

## WorkAdventure

[play.zkm.world](https://play.zkm.world) relies on [workadventu.re](https://workadventu.re/)

## Videoconferences & Hosting

[play.zkm.world](https://play.zkm.world) is hosted at the ZKM | Center for Art and Media. The Videoconferences are provided by [meet.zkm.de](https://meet.zkm.de).
