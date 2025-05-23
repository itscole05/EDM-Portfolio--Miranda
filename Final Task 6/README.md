# Finals Task 6 – MongoDB Practice

##  Task 1: Insert Movies

```sql
db.movies.insertMany([
  {
    title: "Fight Club",
    writer: "Chuck Palahniuk",
    year: 1999,
    actors: ["Brad Pitt", "Edward Norton"]
  },
  {
    title: "Pulp Fiction",
    writer: "Quentin Tarantino",
    year: 1994,
    actors: ["John Travolta", "Uma Thurman"]
  },
  {
    title: "Inglorious Basterds",
    writer: "Quentin Tarantino",
    year: 2009,
    actors: ["Brad Pitt", "Diane Kruger", "Eli Roth"]
  },
  {
    title: "The Hobbit: An Unexpected Journey",
    writer: "J.R.R. Tolkien",
    year: 2012,
    franchise: "The Hobbit"
  },
  {
    title: "The Hobbit: The Desolation of Smaug",
    writer: "J.R.R. Tolkien",
    year: 2013,
    franchise: "The Hobbit"
  },
  {
    title: "The Hobbit: The Battle of the Five Armies",
    writer: "J.R.R. Tolkien",
    year: 2014,
    franchise: "The Hobbit",
    synopsis: "Bilbo and Company are forced to engage in a war against an array of combatants and keep the Lonely Mountain from falling into the hands of a rising darkness."
  },
  {
    title: "Pee Wee Herman's Big Adventure"
  },
  {
    title: "Avatar"
  }
])
```
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/insert.png)

##  Task 2: Querying Documents

- Get all documents
```sql
  db.movies.find()
```
![Alt Text]()

- Get all documents with writer set to "Quentin Tarantino"
```sql
db.movies.find({ writer: "Quentin Tarantino" })
```
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/find.png)

- Get all documents where actors include "Brad Pitt"
```sql
db.movies.find({ actors: "Brad Pitt" })
```
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/find1.png)

- Get all documents with franchise set to "The Hobbit"
```sql
db.movies.find({ franchise: "The Hobbit" })
```
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/find2.png)

- Get all movies released in the 1990s (1990 ≤ year ≤ 1999)
```sql
db.movies.find({ year: { $gte: 1990, $lte: 1999 } })
```
![Alt Text](http://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/find3.png)

- Get all movies released before 2000 or after 2010
```sql
db.movies.find({ $or: [ { year: { $lt: 2000 } }, { year: { $gt: 2010 } } ] })
```
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/find4.png)

##  Task 3: Updating Documents

Update documents in the movies collection as follows:

- Add a synopsis to "The Hobbit: An Unexpected Journey":
"A reluctant hobbit, Bilbo Baggins, sets out to the Lonely Mountain with a spirited group of dwarves to reclaim their mountain home - and the gold within it - from the dragon Smaug."

![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/update1.png)

- Add a synopsis to "The Hobbit: The Desolation of Smaug":
"The dwarves, along with Bilbo Baggins and Gandalf the Grey, continue their quest to reclaim Erebor, their homeland, from Smaug. Bilbo Baggins is in possession of a mysterious and magical ring."

![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/update2.png)

- Add the actor "Samuel L. Jackson" to "Pulp Fiction".

![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/tree/main/Final%20Task%206)

##  Task 4: Text Search Queries
Write queries to:

- Find all movies whose synopsis contains the word "Bilbo".
  
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/findx1.png)

- Find all movies whose synopsis contains "Gandalf".
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/findx2.png)

- Find all movies whose synopsis contains "Bilbo" but not "Gandalf".
  
![Alt Text](http://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/findx3.png)

- Find all movies whose synopsis contains "dwarves" or "hobbit".
  
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/findx4.png)

- Find all movies whose synopsis contains both "gold" and "dragon".
  
![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/findx5.png)

##  Task 5: Delete Documents
Remove the following movies from the collection:

- Pee Wee Herman's Big Adventure

![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/delete1.png)

- Avatar

![Alt Text](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/del2.png)

##  Task 6 – MongoDB Files

[Download MongoDB File](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%206/ft6images/mongo_practice.movies.json)
