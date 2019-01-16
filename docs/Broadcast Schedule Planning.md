# Broadcast Schedule Planning

## Pre-conditions

* There are an equal number of producers and shows
* There are at least 4 shows
* There are enough broadcasters that each show can have 2 - 4 broadcasters

## Constraints

Hard constraints:
* Every show must be 1.5 hours (3 time blocks) and start at the top of the hour
* Shows can only run from 10am to 7:30pm from Monday to Friday
* Every producer/broadcaster cannot be scheduled during their lectures/tutorials/other commitments indicated by them
* Every producer/broadcaster must be in 1 show
* Every show must has 1 producer and 2 - 4 broadcasters


Soft constraints:
* Shows start at even hours (10am, 12pm, 2pm, 4pm, 6pm)
* Shows are not scheduled within 1 hour of each other (e.g. if a show ends at 1:30pm, do not schedule the next show at 2pm)
* There are shows for at least 4 different days of the week
* Producers/broadcasters are not scheduled within 30 min of their schedule (e.g. if their class ends at 2pm, they cannot be given a show before 2:30pm)
* Broadcasters are given shows that they prefer (top 3 - individual ranking of top 3 not considered for now)
* Producers/broadcasters are not assigned a show on their free day unless they live on campus

## Front-End Requirements

Broadcast Director:
* CRUD project
* List all show names/descriptions (manually for now)
* Generate QR code/custom URL for members to fill in
* After all the members have responded, run OptaPlanner to generate the schedule
* Could have a field to get availability for BMT but this doesn't need OptaPlanner, the BD can do it by hand

Members:
* Follow QR code/custom URL to create a new entry for the existing project
* Indicate producer or broadcaster
  * Producer indicates which show they are in charge of
* Indicate if they live on campus (or maybe a box to check if they mind coming on their free day?)
* Collect email to track their identity (URL to edit their entry in the future?)
* Timetable (Mon - Fri, 9am - 9pm) in half-hour chunks
  * Clicking turns the cell red, meaning not available
  * Able to indicate hard/soft schedule in the future?
  * Able to upload calendar file (from Calendar app or NUSMods) to auto block out timeslots in the future?
  * Add note about alternate weeks (if their class is on alternate weeks, they should indicate not available)

