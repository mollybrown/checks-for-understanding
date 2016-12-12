## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR. 

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
 - ActiveRecord is Ruby ORM that allows us to interact with/manipulate data in a database as we would a regular Ruby object.
2. What kind of methods are `belongs_to`, and `has_many`? (i.e. class or instance) Give an example.
 - `belongs_to` and `has_many` are class variables that create association between other models(classes) in ActiveRecord. EX: A Book(model) belongs_to an Author(model), and a Author has_many Books.
3. What do they allow you to do?
 - They allow us to create direct connections between different ActiveRecord models.
4. What's the difference between agile workflow and waterfall method?
 - Agile is based upon iterative build/test/release cycles; waterfall is based on completing each major phase of a project before moving on to the next (non-iterative).
5. What is the difference between `#new` and `#create`?
 - `#new` creates a new object, but does not save it to the database. `#create` creates a new object AND saves it to the database.
6. At a basic level, what does cURL allow you to do?
 - cURL allows us to get and send files over different internet file transfer protocols using the command line.
7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
 - Not sure if this is supposed to be a trick question... A database with only teachers and students is missing the element that actually creates the relationship between teachers and students, i.e. classes. Simply having a teacher model and a student table would be fairly useless in the normal way that we think about the student/teacher relationship.
 - ![Schema Diagram](https://www.dropbox.com/s/hvxuc7p21pddjxh/Screen%20Shot%202016-12-11%20at%209.11.11%20PM.png)
8. Define foreign key, primary key, and schema.
 - Foregin key: Column used to reference the primary key of another table.
 - Primary key: Column used to uniquely identify all table records(rows).
 - Schema: The current structure of the database
9. Describe the relationship between a foreign key on one table and a primary key on another table.
 - The foreign key on one table refers to the primary key of another table.
10. What are the parts of an HTTP response?
 - A status line containing the HTTP version and response code, followed by response headers, follwed by an optional response message body. 
11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.
 - So far I have seen this in the form of extracting logic related to routing out into modules, using view partials, and in taking advantage of model associations to prevent the need for excess ruby code when running db queries. However, none of these are specific to Sinatra, so maybe I am missing something?


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
4. What can you expect from a group as you begin working together? As you continue working together?
5. What two columns does `t.timestamps null: false` create in our database?
6. What cURL flag can you use to send a `POST` request?
7. What case does JSON (and JavaScript) use for multi-word variables?
8. What case does Ruby use for multi-word variables?
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
15. What types of output do we want to test when we test our controllers?
16. What could you see in your code that would make you think you might want to create a partial?
17. Why might you use a helper method?
