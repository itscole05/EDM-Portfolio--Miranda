## Final Lab Task 1 - Events Management DB ##

## Step 1: Create Database ##


Using MySQL workbench, we first create a database umder the name events_db. After that create a events_tbl : this table consist the events_id as the PRIMARY Key and event_name.

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%201/Images4/task%201.png" align="center" height="350" width="600"/>

## Step 2: Create attendees_tbl ##

This table will hold the attendees_id as the PRIMARY Key and also the attendees_name.

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%201/Images4/ATTENDANCE.png" align="center" height="350" width="600"/>

## Step 3: Create events_attendees_tbl ##

This table will links the events_tbl and attendees_tbl using a many-to-many relationship. 

It uses event_id and attendees_id as FOREIGN Keys.

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%201/Images4/image%20(2).png" align="center" height="350" width="600"/>

## Step 4: Create events_sponsors_tbl ##

This links sponsors to events with events_id and and sponsor_name.
<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%201/Images4/image.png" align="center" height="350" width="600"/>

## Here's the Screenshot of the output of my tables ( See screenshot attached)

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%201/Images4/image%20(1).png" align="center" height="350" width="600"/>

## Here's the Screenshot for the EDR (See Screenshot) ##

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%201/Images4/ERD.jpg" align="center" height="350" width="600"/>
