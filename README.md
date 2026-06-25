<img width="12800" height="4340" alt="Logo Standard Landscape Reversed RGB" src="https://github.com/user-attachments/assets/eef220f5-6f30-4c28-b7ce-586399599be9" />

# Course Assignment App Board (CAAB)

This is my project I have completed for INFO102 - Foundations of App Development at Victoria University of Wellington with my teammate, Diksha Patel. It carries the most weight among all graded items. 

You can try this project by accessing it though [this Plunker](https://plnkr.co/edit/tDZRRzbAse6Wasl3).

---

## Project Goals

CAAB need to ensure the app can manage information about courses and workshops/tutorials in a timely and efficient way. The focus for now is on undergraduate courses available in SDT, with a view to expanding it to postgraduate courses at a later date if all is going well. This involves a number of courses that can be added to individual student’s course feeds, where they can also manage their choice of workshops/tutorials.

---

## Project Organisation

CAAB is our client. CAAB needs you to develop a Web application that fulfils their information management requirements. CAAB does not need reports (great!). Instead, they want to see the project rolling from day one—that means using Agile to develop the software. This will help build trust that you can deliver what they need. You are expected to deliver an application that works from day one, and to keep delivering functionality on a weekly basis.

---

## System Requirements 

The following requirements are non-negotiable: 
- The project and resulting application will adopt a client-server architecture. 
- On the server side, a web server will be provided with data that can be accessed using HTTP GET. No work will be done on the server side, and no changes can be done either. 
- Since no changes can be done to the server, in this project you will develop only the client. 
- The client will be a single-page application, i.e. running with a single page load on a browser.  
- The client will run on modern browsers (Chrome, Firefox, Safari) and may even be accessed on mobile phones. 
- The client will be developed with standard web technology: HTML, CSS, and using Python and Vue.js version 2. Note: projects using other languages and toolkits (e.g. JavaScript, Angular, Vue 3) will receive a mark of 0. 

---

## Data Requirements 

- The server maintains a user list with: login name, password. This will be set up for you and cannot be modified. 
- Each course has the following data: ID (unique to each course offering), code (e.g. “INFO102”), name, overview, year, trimester, lecture times, prerequisite (i.e. what other course code must be completed before taking this course, or “” for “no prerequisite”), and options for workshops/tutorials (a list of days and times). Sample data will be provided.  
- Each student has, in addition to a login name and password, the following information recorded:  
a)	a grade point average (GPA);  
b)	a list of courses already (successfully) completed; 
c)	an indication of whether the student is domestic or interplanetary; 
d)	a record of what courses they are currently enrolled in, and, for each course, which of the workshops/tutorials they have selected (which is initially empty, i.e. when a student enrolls in a course they do not have a workshop/tutorial selected); and  
e)	an indication for each course of the enrolment status (see below)

---

## Functional requirements

- There are two main views: the course feed and the course directory.
- The student’s course feed shows the courses in which they are enrolled and allows them to drop courses (subject to the constraints below) and to select and change their choice of workshop/tutorial for a course.
- The course directory shows all available courses and allows students to see course details and to add courses to their enrolment.  
- Options for workshops/tutorials can be (optionally) selected when a course is added, can be selected later, and can be changed. 
- The list of courses can be viewed without logging in, but in order to enroll in a course the user will need to login. 
- When selecting a workshop/tutorial the system should warn the student if they are selecting a session that clashes with their current schedule (i.e. if the time and day is the same as another workshop/tutorial that they have selected (in another course) or with another lecture). 
- When adding a new course the system should check the following conditions and, depending on the condition, either decline to add the course or, if approval is possible, record that approval is required. This means that each enrolment in a course by a student has an enrollment status that can be one of “not requiring approval”, “requiring approval with approval pending”, or “requiring approval with approval having been given”.  
- Course enrolment conditions: (this constrains both adding and dropping courses, for example an international student is not allowed to drop a course if this would bring their enrolment in a given trimester below 2 courses, they must first add another course) 
a)	A student can normally only enroll in 3 courses in each trimester. A fourth course can be added if either the student has a GPA of 7 or higher, or if it is approved by the Associate Dean.  
b)	A student who has a GPA of 4 or lower can only enroll in 2 courses in each trimester.  
c)	An interplanetary student must take at least 2 courses in each trimester. There can be no exceptions (i.e. this requirement cannot be waived by the Associate Dean). 
d)	A student can only enroll in two courses that clash if it is approved by the Associate Dean 
e)	A student can only enroll in a course if they have completed the prerequisite course or if they will have completed it by the time they begin the course. For example, if INFO 101 is a prerequisite for INFO 201 then the student could enroll in INFO 201 in second trimester only if they have already done INFO 101 or are enrolled in INFO 101 in first trimester. This requirement can be waived by the Associate Dean. 
 	 
**Important Notes:**
1.	This is a minimal set of functions required by the client. Other good ideas that improve value are welcomed and will be rewarded. You are invited to add useful functionality to the application. Note however that you cannot change the server behaviour. 
2.	The requirements may change – the client will review progress and new or updated requirements may be made available partway through the course of the project.

---

## Other requirements 
- Forms are easy to use and have good presentation (e.g. clean, with properly aligned fields) 
- Dropdown menus are preferred over empty fields. 
- Forms have pre-selected options whenever possible. 
- Optional challenge: Forms work well on mobile devices. 
