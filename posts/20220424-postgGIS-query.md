%{
  title: " POSTGIS ",
  tags: ["postgres","postgis","ecto"],
  published: true,
  discussion_url: "https://rokkincat.com/blog/2016-9-23-location-based-search-with-ecto-and-postgres/",
  description: """
  Postgis is extension of postgres
  """  
}
---

## What is postGIS?

PostGIS is an open-source extension for the PostgreSQL database that adds support for geographic data. It allows you to store, query, and manipulate spatial data such as points, lines, and polygons.

## Query for postGIS

### To update

UPDATE locations SET location = ST_SetSRID(ST_MakePoint(lon, lat), SRID);

### To find the location
 Now we can find all the locations within a certain radius of a given point using the ST_DWithin function:

 SELECT name FROM locations
WHERE ST_DWithin(location, ST_SetSRID(ST_MakePoint(lon, lat), SRID), radius);

## Reference URL 
   https://rokkincat.com/blog/2016-9-23-location-based-search-with-ecto-and-postgres/
