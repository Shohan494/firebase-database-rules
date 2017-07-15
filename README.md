## firebase-database-rules
#### Basic understanding of how to write the database rules of a firebase application
How to write database rules in firebase application:

###### If you want to have your database 'read' and 'write' access to any user, no matters what, can be anyone who is using the application.

code:

    {
      "rules": {
        ".read": true,
        ".write": true,
      }
    }
    
###### Another example

code:

    {
      "rules": {
        ".read": true,
        ".write": false,
      }
    }

###### So in the above code, it sets the rules that any user who is using the application can read the data but he can not write any data to the database.

###### If you want to have your database 'read' and 'write' access to only who are authenticated users. That means the signed up and logged in users.

code:

    {
      "rules": {
        ".read": "auth != null",
        ".write": "auth != null"
      }
    }

###### The code above - (auth != null) means 'auth is not equal to null'. So basically this piece of code tells us that 'if any user is authenticated, the user can read and write to the database'
