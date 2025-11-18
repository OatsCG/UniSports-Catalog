# UniSports Catalog
#### A catalog of universities' drop-in sports schedules. Used in the UniSports app.

`meta.json` contains metadata for each school, including colours, logos, and their folder ID.

Each school's folder has an `events.json`, and `version.txt` containing the event json's aggregation date.


## Folder Schema
```
.
├── meta.json
├── UTM
│   ├── events.json
│   ├── version.txt
├── MM
│   ├── events.json
│   ├── version.txt

...

```


## `events.json` Schema
```
{
    "categories": [
        {
            "title": String,
            "symbol": String,
            "isChip": Bool,
            "isMedal": Bool
        },
        ...
    ],
    "events": [
        {
            "id": Int,
            "url": String, // URL
            "title": String,
            "description": String,
            "image": String, // URL
            "start_date": String, // Date String %Y-%m-%d %H:%M:%S
            "end_date": String, // Date String %Y-%m-%d %H:%M:%S
            "venue": String,
            "ticket_label": String,
            "ticket_url": String, // URL
            "sortCategory": String,
            "symbol": String,
            "featuredDecal": String,
            "womens": Bool,
            "lgbt": Bool,
            "bipoc": Bool,
            "intramurals": Bool,
            "closure": Bool,
            "weeklyRepetitions": [String] // su, mo, tu, we, th, fr, sa
        },
        ...
    ],
    "featured": [
        {
            "id": Int,
            "url": String, // URL
            "title": String,
            "description": String,
            "image": String, // URL
            "start_date": String, // Date String %Y-%m-%d %H:%M:%S
            "end_date": String, // Date String %Y-%m-%d %H:%M:%S
            "venue": String,
            "ticket_label": String,
            "ticket_url": String, // URL
            "sortCategory": String,
            "symbol": String,
            "featuredDecal": String,
            "womens": Bool,
            "lgbt": Bool,
            "bipoc": Bool,
            "intramurals": Bool,
            "closure": Bool,
            "weeklyRepetitions": [String] // su, mo, tu, we, th, fr, sa
        },
        ...
    ],
    "announcements": [
        {
            "id": Int,
            "title": String,
            "body": String, // Markdown decorated
            "type": Int // 0=>normal, 1=>closure, 2=>update
        },
        ...
    ]
}
```
