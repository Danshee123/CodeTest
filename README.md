# CodeTest

I have gone throught the code and my thought about the code is it is ok. 
I have refactored some of the code and I think it can be refined much more. 
Like alot of loops and checks are there which can be handled using laravel collection methods which makes laravel more beautiful.we can use a bit of functional programming with the methods that Eloquent gives us.
The main issue I have found is more interative way of coding not the functional style of coding.
The issue here is that if someone has to come back to this method later for a bugfix or a changed requirement, your teammate (or even yourself) is going to "compile" this foreach in his head before doing anything. And in case of checks has he will have to dry run all the code to help getting the understanding of what this code is doing. 
While in functional Programming or using collection methods it helps us to just read the code in simple english and we can get understanding of what is going on here .
Like what I have done in refactoring is in BookingRepository line#463-470 where you were checking translator town and was unsetting(which itself is a costly processs) the value in case of check. I just looped through the collection and using laravel's filter method just got all the jobdis where checktown job->customer_physical_type is not yes. In this case I didn't have to unset the values and also the other programmer can just read through the code in simple english(functional way) and can get the understanding what the code is doing.

