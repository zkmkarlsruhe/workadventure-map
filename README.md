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

## Interactive layers

You can trigger actions if players cross tiles on a specific layer. The actions are ste layer-wise, so even if your action is only on one tile it needs an individual layer.

### Enter the map

Create a layer named `start` with at least one tile. Users joining this map will be randomly placed on any tiles in this layer.

### Exit the map

_ToDo_

### Open websites

Use the following custom properties:

* `openWebsite` (string) with the URL to the website
* `openWebsiteTrigger` (string). If set to `onaction`, the website will not open automatically and the user will see something like 'Press space to open'.

_Note_: Check if the website allows to be embedded. Website can forbid this using the `X-Frame-Options` header.

#### Add a YouTube video

Use the Youtube embed links. They look like this `youtube.com/embed/<video_id>`.

### Play Audio

Use **one** of the following properties:

* `playAudio` (string)
* `playAudioLoop` (string)

Both strings hold an URL pointing to an MP3 file to play. The URL can be realtive to the map file, so you could organize your audio files in a subdirectory like `audio/`.

### Join a Jitsi Meeting

Use the following custom properties:

* `jistiRoom` (string) the Jisti room name
* `jitsiTrigger` (string). If set to `onaction`, the website will not open automatically and the user will see something like 'Press SPACE to enter'.

_Note_: if your Jitsi server automatically mutes user on entering the room it can be offputing for users in this context since they will need to manually unmute themselves. To override this add `#config.startWithVideoMuted=false&config.startWithAudioMuted=false` after the room name.

### Silent zones

Users on the tiles of this layer will not engage in conversations if next to each others.

Set the follwing custom layer property and activate it:

* `silent` (bool)

## Create your own tiles

Tiles are PNG images divided in a 32x32 pixel grid. It is not possible to use other grid sizes (e.g. 16x16). Check out the example tile files in the `public/tiles/` folders.

# Deploy the map

## With Gitlab Pages

The `.gitlab-ci.yml` file in this repository automatically deploay the contents of `public/` after each push. The URL can be found under Settings -> Pages.

If the repository belongs to the user `loelkes` and is named `awesome-map` the URL will be `loelkes.gitlab-pages.zkm.de/awesome-map/`

Open your map with `play.zkm.world/_/global/<link to the map.json>`, in this example `play.zkm.world/_/global/loelkes.gitlab-pages.zkm.de/awesome-map/map.json`.

# Behind the scenes

## WorkAdventure

[play.zkm.world](https://play.zkm.world) relies on [workadventu.re](https://workadventu.re/)

## Videoconferences & Hosting

[play.zkm.world](https://play.zkm.world) is hosted at the [ZKM | Center for Art and Media](https://zkm.de). The videoconferences are provided by [meet.zkm.de](https://meet.zkm.de).
