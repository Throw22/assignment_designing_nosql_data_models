You're building a backend for a university that requires students to be able to login. Once logged in, the students can view the exam grades for their classes. They should be able to view results by semester. Each semester should only show the classes in which that student is enrolled that semester.

user {
  name: string (only word characters)
  email: string (regex for @universityname.edu)
  password: string (length requirement)

  semester {
    'winter2016': [ classResultId, classResultId ]
  }
}

classResult {
  id
  classId
  className
  grades {
    studentId: grade
  }
}
