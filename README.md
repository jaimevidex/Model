# Model — University Domain Model in Java

A small object-oriented domain model of a university, written to practise **inheritance, abstract classes, enums and associations** in Java.

## What's modelled

| Type | Role |
|---|---|
| `UniversityMember` | Abstract base for everyone in the institution |
| `Student` | A member enrolled in course executions |
| `Emplyee` | Abstract base for staff |
| `Support` | Non-academic staff member |
| `Course` | A course, with a semester and a set of executions |
| `CourseExecution` | A concrete run of a course in a given semester |
| `ERole` | Role enum (e.g. student, teacher, staff) |
| `ESemester` | Semester enum |

The point of the exercise is the *relations*: members are associated with course executions through roles, courses aggregate executions, and the two member hierarchies share a common abstract root.

## Structure

```
UniversityMember.java   abstract root of the member hierarchy
Student.java            student member
Emplyee.java            abstract staff member
Support.java            support staff
Course.java             course + semester
CourseExecution.java    one execution of a course
ERole.java              role enum
ESemester.java          semester enum
```

## Build

```bash
javac *.java
```

There is no `main` — this is a modelling exercise, not a runnable application. Open the sources to see the class hierarchy.

## Notes

- Written for the *Programação Orientada a Objetos* course at Instituto Superior Técnico.
- `Emplyee` is spelled as in the original submission; it is kept to preserve the code as handed in.
