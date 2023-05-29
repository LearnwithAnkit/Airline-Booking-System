Airline Booking Backend

Objective:

We need to build a backend system that can support different features for an airline company.
Our end user is going to be someone who wants to book flights and query about flights so we need a robust system to actually help them give the best experience possible.This doc is going to focus on the backend part of the system.We want to prepare the whole backend keeping the fact in mind that the code base should be as maintainable as possible.

Requirements:

Functional Requirements:

A User should be able to search for flights from one place to another.

-User should be able to mention the source and destination details.

-User should be able to select the date of the journey. -[V2] User should be able to search for return flights and multi-city flights.

-User should be able to select the class of flights.[Non-Mandatory]

-User should be able to select the no the seats that they want to book.[Non-Mandatory]

-Now based the above data,we will list down the flights

-We should show our user the best available flight based on the time and
then based on the price.

-We need to support pagination so that we can list chunk of flights at one
point of time.

-We should support the filter of flights based on the price,departure,duration. -[V2]we can add more filters.

A User should be able to book a flight considering the user is registered on the platform.

-User Should be able to cancel the flight, and then based on some criteria
We can initiate the refund.

-User should be able to request and book excess luggage for every flight.
For making a booking, the user has to make a payment(dummy).

Tracking flight prices should be possible, the user should be notified about any price drops or any delays.
User should be able to list their previous and upcoming flights.

User should be able to download the Boarding pass if they have done online check-in.
Online check-in mechanism should be supported.

Notification via email for completing the online check-in before 3 hours of departure.

User should be able to review the flight journey if and only if they have booked a flight.

-Review mechanism should involve star rating along with a comment.

-While listing any flight we should also display the review of the flight.

User should be able to authenticate to our system using email and password.

-[V2]Support Ticketing, where user can raise their queries. 

- Listing FAQ which will be static data - Coupons for discount offer.

Non-Functional Requirements:

We can expect that we are going to have more flight searches than flight bookings.

The system needs to be accurate in terms of booking.

Expect that we will be having approx 1,00,000 total users,5,00,000 bookings might come up in one quarter.

So in one day we can expect 5000 bookings.

System should be capable of scaling up to at least 3x the current estimated traffic.

The System should handle real time updates to flight prices,before user makes the funal booking.

Capacity Estimation-

-Storage estimation-

-For upcoming 5 Years,80,00,000 bookings,2,00,000 Users.Considering all the
User records and booking records take 10 MB of data,the overall 10 TB of memory should be fine for our initial pilot run.

-Traffic estimate-
If we consider 30:1 as the search:booking ratio,then at max we expect
150000 search queries a day.
