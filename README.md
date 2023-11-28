# Rawad-Medeventus-test
This is a task to test your skills in both backend and frontend development using Laravel framework

# User Points System (Loyality)
The project is a website that sells events online. It is required to have points system for users, so they can collect points and use them later for discounts or gifts,etc...

# Details
1. You have to create a new Laravel project
2. We have two types of users:
   
   a. Admin: who can create the events and control the settings related to points
   
   b. Guest: general user who can register and buy events from the website

   
3. Database, Relations, and Migrations:
   
   <b>a. Events:</b>

   They are created by admins and have the following fields:
  
       id(PK)
       title(string, required)
       description(string, optional)
       image(mimes:jpeg,png,jpg,zip,pdf, max:2048, required)
       price(unsignedBigInteger, required, deafault is zero when event is free)
       user_id(FK references id in users table (the id of the admin who created the event))
       
   <b>b. Orders:</b>

    contains users orders
    
        id(PK)
        user_id(FK) references id in users(the id of the user who bought the event)
        timestamps are needed
        payment_id (string related to payment gateway, by now, just give it deafult with this string 123456789)
       
   <b>c. Points:</b>

    contains user points
    
        user_id(FK) references id in users(the id of the user who bought the event)
        points(unsignedBigInteger) will contain the number of points the user collected
        created_at(timestamp) contains timestamp of first added points (this will be used to track points expiry date)

<p></p>

4. Points Settings:
  
    - You have to create Points Settings Form using any frontend framework you prefer(React, Vue JS, ...)
        <i>Note: The image of the form required is uploaded in forms folder</i>

    - You can use any solution you prefer to save these settings on form submit, so they can be used in the project as defined by the admin

<p></p> 
    
5. Test and Code:

    a. Create a very simple Create Event Form for the admin and add new event
        <i> Note: it is needed to consider validation on user inputs. </i>
    

    b. Create a simple page for the guest user to buy the added event, checkout and place order
    <i> Note: On checkout, show the user the total number of points he has and their expiry date</i>
    

    Add the logic and code with your favorite code design and structure so the system is working as required.
   
   <b> Note: It is preferred to include feature tests that you find imporant for the added features explained in the task</b>
   


