Process of organizing data in database. Aimed at improving performance, making database more flexible by eliminating redundancy. Most commonly 3 normalization forms used (2 more exist but are not used in production as much, only for perfect database).

### First normal form
- atomicity of values (i.e. city, street, postal code in each separate row instead of one named *address*)
- separate table for each set of related data (+ primary key)

### Second normal form
- separate table for sets of values that can apply to multiple records
- use them with foreign keys

### Third normal form
- eliminate values that are not dependent on primary key


https://learn.microsoft.com/en-us/office/troubleshoot/access/database-normalization-description
