ThingsHelper
============

Series of AppleScripts I use to automate Things by Cultured Code

Assumptions:
  - You use Things
  - You use (many) repeating tasks to stay on top of things
  - You have relatively predictable phases to your day

The problems these scripts solve for me:

  - I find it daunting when my Today list starts out with more than 10-15 items.  Daunting lists are tempting to ignore.
  - I find it annoying when I'm away from my computer for a day or two and come back to find duplicated items.

Since my Today list was being easily overwhelmed, I wanted to automate it's organization to reflect a concise list of relevant tasks for any point in my day.  

Preface: 
Your day will be different than mine.  
My hope is that by sharing my solution, I might be able to give people a jumping off point for their own automation.
I gotta say, I'm not interested in customizing anybody else's automation.

With that said, here's how I put these scripts to work for me:

crack_of_dawn.scpt
  - Runs at 4:00am, triggered by an appointment in iCal
  - This script:
    - Moves all generated recurring tasks from Today to Next
      - Hides the clutter
    - Moves all tasks tagged "first_thing" to Today
      - My list includes: 
        - meditation (start the day with a clear mind)
        - create something (be a creator, not a consumer)
        - body weight circuit (get the blood flowing)
  - Result:
    - A concise list of things that jumpstart my day
  - My last 'first_thing' is a cold shower.
    - Gets me ready for a morning full of work

shower_complete.scpt
  - I trigger this script manually (through Alfred) after my shower because the timing of that is highly variable.
  - This script:
    - Moves Next tasks tagged 'work' to Today (on weekdays)
    - Moves tasks tagged 'passion', 'morning', and 'goal' 
    - Will selectively hide tasks tagged with a specific day
      - ie, you tag a task 'Tuesday', it won't show up 'Monday'
  - Basically, I tag my important stuff morning because that's when I'm most productive.

lunch_break.scpt
  - Triggered by appointment in iCal
  - I'm not the same without exercise, so it's my focus at lunch time.
  - This script clears all of my tasks and replaces them with tasks labelled 'body_break'.  
    - Hat tip to Hal Johnson and Joanne McCleod 
      - Canadian rock stars of life long fitness

lunch_is_done.scpt
  - I trigger this manually (through Alfred) when I'm done with my exercise
  - This script:
    - Moves tasks tagged work, passion, goal, afternoon, errand, etc to my Today list
  - I tag a lot of my monotonous recurring tasks 'afternoon' because I'm generally less productive in the afternoon
    - I work from home, so this is when I want to put laundry through, cycle the dishwasher, take down garbage, etc.

wind_it_down.scpt
  - Triggered by iCal appointment at 4:30pm
  - As the name implies, I like to take it easy in the evening
  - At this time of day, I'm done with work and want a list of fun/evening-y things to do
  - This script:
    - Moves daytime specific tasks from Today to Next
    - Adds tasks tagged evening, goals, fun, etc to Today
      - Filters new tasks to be day of week specific
  - Whenever I find compelling articles/videos during the day, I like to save the link as a task and tag it evening.
  
eod_clean_up.scpt
  - Triggered by iCal appointment just before midnight
  - As I mentioned above, I hate how recurring tasks pile up on days when I'm not around to clear them up.
  - This script:
    - Moves tasks shown by wind_it_down.scpt back to Next
    - Deletes all tasks tagged _r, my way of identifying recurring tasks
    - Cleans out the Logbook (I'm not one that draws any satisfaction from reviewing ticked off lists)



So that's it, that's all.  To sum up, I've been happy with how this solution keeps me focused on what's important at the right times of day while never having to lose sight of all those crazy "I should learn Java" type tasks.  Everything has its place.

If you read this far, you're a nerd, and I love you for it.

I hope this proves useful for you.





