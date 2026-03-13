# 13 MAR - Friday Courses

## JPA Overview

### Jakarta Persistence API
- defines a common APU for object-relational mapping frameworks like Hibernate
- abstract away database translation logic between different databases

### ORM
- Object Relational Mapping
- define relationships between tables in your classes
- Update multiple tables in a single transaction/ command

### do we use spring JPA and Hibernate?
- To access it we need to add the JPA dependency
- With an existing database connection we update the application.yaml file
- Some relevant annotations:
  - @Entity
  - @Id
  - @GeneratedValue
  - @Column
  - @Repository

# Usefule Commands
- lsof -i:(port number)
- kill -9 12345(process id)