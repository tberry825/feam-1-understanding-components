
 Using the image of the Airbnb UI, answer the following questions:
 1. What are four main components you see on the page?
    a. NavBar
    b. SearchBar
    c. Type of AirBnB Bar
    d. AirBnb Info (picture, location, views, available time, price)

 2. Put the components in order to show the parent/child relationship. So if component x is the mother of y and grandmother of z, you would write: 
    1. x
    2. y
    3. z

    a. Parent - AirBnb component / app.js
    b. child - 
        a. NavBar
        b. SearchBar
        c. Type of Listing Bar
        d. Listing (picture, location, views, available time, price)


3. Which component needs access to every piece of data? Which component only needs access to the filtered data? 
     - The parent needs access to every piece of data. 
     - the choice between filtering data in the parent or child component depends on your application's structure. 
      -- it might be necessary for both the parent and child components to have access to filtered data. (if the filtered data needs to be displayed in multiple child components with different filtering criteria. )


4. What are three different key/value pairs that will be needed for each listing?
    a. price
    b. location
    c. views
    d. availavle time


5. What JavaScript could we write to filter the objects based on whether or not the listing has a pool?

filter the Listing array object: .filter(), with an if statement
const airbnbListings = [
  { id: 1, title: "Amazing Views Airbnb", hasPool: true, amazingViews: true, beachfront: false, lakeFront: false },
  { id: 2, title: "Beachfront Paradise", hasPool: false, amazingViews: false, beachfront: true, lakeFront: false },
  { id: 3, title: "Luxury Lakefront Villa", hasPool: true, amazingViews: false, beachfront: false, lakeFront: true },
  // ... more listings
];

function filterListingsWithPool(listings) {
  const listingsWithPool = listings.filter(listing => {
    // Check if the listing has a pool
    return listing.hasPool;
  });

  return listingsWithPool;
}

const filteredListings = filterListingsWithPool(airbnbListings);
console.log(filteredListings);
