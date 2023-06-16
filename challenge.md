# Challenge: Creating Our dev.to Article

#### STEP 01

**Create dev.to account**

#### STEP 02

_Login and click create a post_

#### STEP 03

~~Start create the article~~

> Tips kaya raya dari mbah google

![gambar dari google](https://asset.kompas.com/crops/UOGoI_KgW8TOoyT9jQBvMaVtjoo=/0x0:750x500/1200x800/data/photo/2022/11/05/6365d2c9b2be9.jpg)

Gambar nya berhasil dimasukan

```ts
/**
 * Generates random latitude and longitude within a given distance from the specified coordinates.
 * @param {number} lat - The latitude coordinate.
 * @param {number} lon - The longitude coordinate.
 * @param {number} distance - The distance in kilometers.
 * @returns {Array<number>} - An array containing the random latitude and longitude.
 */
function getRandomCoordinates(lat, lon, distance) {
  const EARTH_RADIUS = 6371.0; // Radius of the Earth in kilometers

  // Convert latitude and longitude to radians
  const latRadians = (lat * Math.PI) / 180;
  const lonRadians = (lon * Math.PI) / 180;

  // Convert distance to radians
  const distanceRadians = distance / EARTH_RADIUS;

  // Generate a random bearing (in radians)
  const bearing = Math.random() * 2 * Math.PI;

  // Calculate the new latitude
  const newLatRadians = Math.asin(
    Math.sin(latRadians) * Math.cos(distanceRadians) +
      Math.cos(latRadians) * Math.sin(distanceRadians) * Math.cos(bearing)
  );

  // Calculate the new longitude
  const newLonRadians =
    lonRadians +
    Math.atan2(
      Math.sin(bearing) * Math.sin(distanceRadians) * Math.cos(latRadians),
      Math.cos(distanceRadians) - Math.sin(latRadians) * Math.sin(newLatRadians)
    );

  // Convert new latitude and longitude to degrees
  const newLat = (newLatRadians * 180) / Math.PI;
  const newLon = (newLonRadians * 180) / Math.PI;

  return [newLat, newLon];
}
```

| Header 1 | Header 2 | Header 3 |
| -------- | -------- | :------: |
| Cell 1   | Cell 2   |  Cell 3  |
| Cell 4   | Cell 5   |  Cell 6  |
