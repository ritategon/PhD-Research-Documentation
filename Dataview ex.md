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


<iframe src="/locations.html" width="100%" height="600"></iframe>





```dataviewjs
dv.paragraph("### Locations Table");

const pages = dv.pages('"Documentation/Locations"')
  .where(p => p.geographical_data)
  .sort(p => p.geographical_data.name, 'asc');

let tableRows = pages.map(p => [
  p.geographical_data.name || '',
  p.geographical_data.description || '',
  p.geographical_data.certainty || '',
  p.geographical_data.coordinates || ''
]);

dv.table(
  ["Name", "Description", "Certainty", "Coordinates"],
  tableRows
);
```
