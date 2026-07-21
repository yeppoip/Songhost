to host a song do it like this first use this json template 

```json
{
  "id": 900002,
  "name": "Notion",
  "artist": "The Rare Occasions",
  "download": "https://raw.githubusercontent.com/yeppoip/Songhost/main/Music/Notion.mp3",
  "hash": "189155f567873a277e17e7e4a438dd537e09e6b80b26ae2569b105e119e3f540"
}
```

then put it like this

```json
{
  "songs": [
    {
      "id": 900002,
      "name": "song",
      "artist": "artist",
      "download": "https://raw.githubusercontent.com/yeppoip/Songhost/main/Music/whateversong.mp3",
      "hash": "256hash"
    },
    {
      "id": 900003,
      "name": "Notion",
      "artist": "The Rare Occasions",
      "download": "https://raw.githubusercontent.com/yeppoip/Songhost/main/Music/Notion.mp3",
      "hash": "189155f567873a277e17e7e4a438dd537e09e6b80b26ae2569b105e119e3f540"
    }
  ]
}
```

for the id make sure its plus one every song 

---

## Getting the hash

on BOTH operating systems use:

```
cd
```

then go to your file explorer, open the folder where the song is placed, copy the path, and paste it into your terminal.  
it should look like this:

```
cd /path/to/your/song
```

---

## Windows (PowerShell)

Use PowerShell to generate a SHA‑256 hash:

```powershell
Get-FileHash .\YourSong.mp3 -Algorithm SHA256
```

The hash will appear under the **Hash** column.

---

## Linux (Fedora, Ubuntu, Arch, etc.)

Use `sha256sum`:

```bash
sha256sum YourSong.mp3
```

The output will look like:

```
3f2a9c8b7e1d0c...c91f  YourSong.mp3
```

Copy the long hash (the part before the filename).

and then paste it into the hash section of index.json
Make sure to add the song to the Music folder of the github
