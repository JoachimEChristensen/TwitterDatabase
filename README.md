# Twitter Database
## How it works
This program was not finished in time as I had issues with wrapping my head around how to query using MongoDB, as well as actually setting the DB up.

However, I will attempt to explain how I imagine the functions would work.

### How many Twitter users are in the database?

To get the users from the database, you use an aggregate function to group all the unique users together, then you grab a length on the aggregated users.

### Which Twitter users link the most to other Twitter users? (Provide the top ten.)

Grouping all the users together gives you every time that user is mentioned. further cutting every NO QUERY tweet from the grouped users will give you each time that user mentiosn another user. Just a matter of sorting and limiting the query from that point.

### Who is/are the most mentioned Twitter users? (Provide the top five.)

This time we remove all the NO QUERY entries and group the mentioned users together, by targeting the actual tweet and seeing if a user's name is mentioned. Resulting collection would likely be limited by 5.

### Who are the most active Twitter users (top ten)?

We do the same thing as in the linking query, except this time we take every single query and see how many tweets every user has. Then, we limit by 10 and sort to find the top 10.

### Who are the five most grumpy (most negative tweets) and the most happy (most positive tweets)?

Group all the users together based on negative tweets, gather those with the most negative tweets limited by 5 and present them after sorting. Then, do the same but for happy tweets, and append it to the text box to show both sides.

## How to use

To build the project, you will need Maven installed as it is integrated into the program.

Given that the program wasn't finished, you can't exactly run it, but if you could, you would just run the program from your relevant IDE (Netbeans in my case) to activate the UI.

## Issues

The actual program isn't done and I merely tried to explain how I would presumably do the queries.

I have a hard time trying to wrap my head around querying with MongoDB.
