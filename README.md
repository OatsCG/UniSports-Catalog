# Drop-In Sports Catalog
#### A catalog of university drop-in sports schedules that support the Drop-In Sports app.


## Schema
```ts
{
  "catalog": [
    {
      "title": String,
      "icon": String, // Image URL
      "version_url": String, // .TXT URL
      "schedule_url": String // .JSON URL
    },
    ...
  ]
}
```
