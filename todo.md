# To Do
*Last Updated: 12/11/18*

## Features: 
- [ ] work on UT Planner
- [ ] work on multiple schedules
- [ ] polish
- [ ] clean upcalendar export and add more options to screen
- [ ] maybe show how many people have a class in their cart
- [ ] more 'at a glance info'

## Known Bugs:
- [ ] Fix the update/install bug

## Completed:
- [x] unneeded Logout message on individual course pages
- [x] RMP not working on individual course pages
- [x] Textbook button (amber)
- [x] Calendar popup
- [x] online classes no times in popup link 
- [x] load all courses on first pages
- [x] Location in popup extra info
- [x] Export calendar format 
- [x] import courses from class schedule screen
- [x] all semester's grade distribution
- [x] import into and export from UT registration plus
- [x] Showing the icon on the flags pages
- [x] Easter egg, no course messages
- [x] search by unique number

for FIXING DB: 

ALTER TABLE agg ADD semesters

update agg
set semesters = (select group_concat(sem) from grades where agg.prof = grades.prof and agg.course_nbr = grades.course_nbr and agg.dept = grades.dept);
