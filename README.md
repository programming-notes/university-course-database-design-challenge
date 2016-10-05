# University Course Schema Design 
 
## Summary 
We're going to design a database schema that would support a university course enrollment application.  Imagine an application where students are able to browse the university's course offerings.  Each of the university's courses is listed:  English 101, English 201, Math 101, etc.  Students browse the list and enroll in courses.  The specific requirements are presented in the releases.


## Releases
### Release 0: Basic Schema
Begin by designing a database schema based on the requirements listed below.  Use [Schema Designer][] to visually represent your schema.

- A student can enroll in many courses.
- A course can have many enrolled students.
- A student receives a final grade for each enrolled-in course (think carefully about what table this data lives in).
- A course is taught by one teacher.
- A teacher can teach multiple courses.


### Release 1: Updated Requirements
The requirements for our schema have changed.  Our database needs to support some additional functionality.  Modify the schema design to match the requirements listed below.

- A department offers many courses.
- A course is offered by one department.
- A course has many sections (e.g., English 101, Section 1; English 101, Section 2, etc.).
- A section is offered either Monday/Wednesday/Friday or Tuesday/Thursday.
- A section has a start time and an end time.
- A student attends a course by enrolling in a specific section of the course.
- A student receives a final grade for each enrolled-in section.
- A section is taught by one teacher.
- A teacher can teach multiple sections.


###Release 2 : Enforcing time constraints

How would you enforce time constraints?  For example, students can't attend and teachers can't teach two sections whose times overlap.

With your pair, talk about how you'd do this.  Hint: you might want to use a whiteboard.

Are you able to infer if student and teacher data violate this constraint?  Even if the database itself doesn't have this constraint built in, if you can infer a violation, you could conceivably write ruby code to ensure this violation doesn't occur.  

What are the potential costs if you are relying on supporting ruby code to help validate your data?  Write an explanation in your gist.

#### Cross-listing classes

Sometimes schools allow courses to be cross-listed in multiple departments.  For example, a Combinatorics class might be in both the Mathematics and Computer Science departments.  

How would you alter the schema above to accommodate that?

When you are done, take a screenshot of your final schema design, and commit it.

<!-- ##Optimize Your Learning  -->

## Conclusion

[Schema Designer]: https://schemadesigner.devbootcamp.com/
