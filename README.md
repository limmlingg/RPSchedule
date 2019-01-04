# RPSchedule
RPSchedule is currently under development and is not ready to be used. Basic features will be completed by Aug 2019.

## Objectives
* Make broadcast scheduling easier for Radio Pulze
* Learn database

## Requirements
### Features
* Login for admins.
* CRUD projects for admins.
* Projects have a title, a description (optional) and type (focusing on weekly schedules).
  * Other project types will be considered once the basic features are completed.
* Admins can generate a URL/QR code to send to members.
  * This URL/QR code is based on the hash of the project (created when the project is first created) so it will not change even if the project details change.
* Members access the URL to enter the times which they are free. This data is stored in a database.
* Admin can generate a schedule based on members data.
  * Might be using OptaPlanner
* Admin can save generated schedule to their local disk.

## Contributing
I am not accepting contributions right now as the project is very early in its development stage. I will welcome bug reports and pull requests when basic features have been implemented.
