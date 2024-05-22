---
layout: post
title: University Webpage Project
subtitle: A functional application and course registration university page
cover-img: /assets/img/path.png
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [SQL, Flask, Python, AWS]
---

https://github.com/yusefjawad03/uni-webpage

Utilizing Python, Flask, and MySQL, this university webpage which was completed as a group of 3 emulates the functions of a university webpage with a Minecraft theme, allowing users to apply to the university (inputting all necessary information), and allowing faculty with separate user-specific accounts to accept or reject these students. Then, accepted students can pay their deposit, subsequently register for courses, and engage in other features such as a chat room and rating professors. Images of the webpage can be found in the final-report.md file.

Desgin Features:
Navigation bar: Allows the user to return to their "home" page at all times, access their personal information page, and quickly log out.

We split some routes/modules (like user management, transcripts, and student management) into their own files/Blueprints to increase readability of our code, maintain consistent URL structures, more easily identify errors, and collaborate on code better.

In an effort to reuse as much code as possible, we created a base HTML template that was included on (almost) every other template. We also tried to use macros wherever possible to save modularize our HTML as much as possible.

This decision also affected how user roles with more permissions (such as grad secretaries and sysadmins) access different functiions of the system; rather than having one list of all users with specific functions for each user based on the user type, they access different index pages for different functions (i.e. alumni list vs. student list vs. user list).

We used Bootstrap as our styling framework so that we could spend the majority of our time developing functionality and not as much defining custom styling to make our advising system user-friendly. We also used DataTables to improve our tables (to allow for searching/pagination/sorting).
We added client-side validation to forms wherever possible so as to give users more descriptive feedback on their inputs before submitting the form data to the back-end. (Validation, often more in-depth, was also done on the back-end.)

The applications page was mainly just the front of the website and most additions were made for the applicant user type, with some being added to existing faculty and gs users

It was assumed anyone could access the recommendation letter page as long as they had the email that a letter had been requested of. It was also assumed that the transcript for applicants does not affect them as students, and that the transcript for applicants is simply just marked as received or not received in the system.

We had to adjust the course table from reg as it stored prereqs in a way that vialoated normal form, so we created a prereq table for a many to many relationship
We had to make some considerations about account type, we do not allow a user to have multiple roles. we believe this may not be the most efficent method but it makes leakage and edge case errors less possible. with the time we had, we believe this was neccesary.

Aditional Features:

Alumni Chatroom:
The alumni chatroom enables graduated students to chat to eachother. The messages are stored through the databse which lets each user logged on the chat to be able to see what is happening in conversation.

Student-Student and Professor-Student Messaging:
Students can click view classmates to see their classmates, the student can then click the message button next to all of their classmates to message them indivudally, which they will receive in thre inbox. A professor can also see a list of their students and message them as well.

Rate My professor/courses:
Students can look at their previous professors/courses from their home screen. They can rate each of them out of 5 and leave a comment.
The course list and professr list now have buttons that show the professors/courses ratings
