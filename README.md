# rainlink-spotify
A rainlink plugin that allows you to play music on spotify

Install
```
npm i rainlink-spotify
```

Support source:
```
- https://open.spotify.com/track/7nw4ElerVAP5235FN5D2OI
- https://open.spotify.com/playlist/2gzszlY4WeJOTOUU6x3sgA
- https://open.spotify.com/album/18UoCkfQKlMVnAcZXbiBz8
- https://spotify.link/zu1pVRAg6Db
- https://open.spotify.com/artist/64tJ2EAv1R6UaZqc4iOCyj?si=mxc5IMM9RQeEPmY0KBIfjg
```
How to
```js
const { Rainlink } = require('rainlink');
const { SpotifyPlugin } = require('rainlink-spotify');

const rainlink = new Rainlink({
    library: new Library.DiscordJS(client),
    nodes: Nodes,
    plugins: [
      new SpotifyPlugin(
        clientId: "your_spotify_client_id",
        clientSecret: "your_spotify_client_secret",
        playlistPageLimit: 1,
        albumPageLimit: 1,
        searchLimit: 20,
        searchMarket: "US"
      ),
    ],
});
rainlink.search(`https://www.spotify.com/us/playlist/53362031`); // track, album, playlist
rainlink.search('mirror heart', { engine: 'spotify' }); // search track using spotify
```