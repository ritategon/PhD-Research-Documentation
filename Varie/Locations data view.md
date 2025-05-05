
```dataview
TABLE
  geographical_data.name AS "Name",
  geographical_data.description AS "Description",
  geographical_data.certainty AS "Certainty",
  geographical_data.coordinates AS "Coordinates"
FROM "Documentation/Locations"
WHERE geographical_data
SORT geographical_data.name ASC
```



```dataview
TABLE
  geographical_data.name AS "Name",
  geographical_data.description AS "Description",
  geographical_data.certainty AS "Certainty",
  geographical_data.coordinates AS "Coordinates",
  geographical_data.pleiades_id AS "Pleiades ID"
FROM "content/Locations"
WHERE geographical_data.certainty = "Confirmed"
SORT geographical_data.name ASC
```

```dataview
TABLE
  geographical_data.name AS "Name",
  geographical_data.description AS "Description",
  geographical_data.certainty AS "Certainty",
  geographical_data.coordinates[0] + ", " + geographical_data.coordinates[1] AS "Coordinates",
  "[" + geographical_data.pleiades_id + "](https://pleiades.stoa.org/places/" + geographical_data.pleiades_id + ")" AS "Pleiades Link",
  "[View on Google Maps](https://www.google.com/maps?q=" + geographical_data.coordinates[0] + "," + geographical_data.coordinates[1] + ")" AS "Map"
FROM "content/Locations"
WHERE geographical_data.certainty = "Confirmed" AND geographical_data.coordinates[0] != null
SORT geographical_data.name ASC
```




```dataview
TABLE
  geographical_data.name AS "Name",
  geographical_data.description AS "Description",
  geographical_data.certainty AS "Certainty",
  geographical_data.coordinates[0] + ", " + geographical_data.coordinates[1] AS "Coordinates",
  "[" + geographical_data.pleiades_id + "](https://pleiades.stoa.org/places/" + geographical_data.pleiades_id + ")" AS "Pleiades Link",
  "[View on Google Maps](https://www.google.com/maps?q=" + geographical_data.coordinates[0] + "," + geographical_data.coordinates[1] + ")" AS "Map"
FROM "content/Locations"
WHERE geographical_data.certainty = "Confirmed" AND geographical_data.coordinates[0] != null
SORT geographical_data.name ASC
```

## Locations

| Name | Coordinates | Description | Certainty | Pleiades ID | Heracles Context |
|------|-------------|-------------|-----------|-------------|------------------|