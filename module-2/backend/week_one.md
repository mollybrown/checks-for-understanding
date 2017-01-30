## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
 - GET: Ask the server for a resource.
 - POST: Submit data to the server.
 - PUT: Create or update (in whole) a resource on the server.
 - PATCH: Update (in part) a resource on the server.
 - DELETE: Destroy a resource on the server.
2. What is Sinatra?
 - Sinatra is a DSL which responds to HTTP requests and is used for web development.
4. What is MVC?
 - MVC stands for model-view-controller, which is a pattern for creating user interfaces for an application. The model contains the data and logic for the application, the view renders the output for the user, and the controller manages changes to the model and view based on user input.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
 - So that other people can know what our application is doing quickly and without exessive explanation needed.
6. What types of variables are accessible in our view templates without explicitly passing them?
 - Instance variables.
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?


 ```ruby
  get '/horses' do
    erb :index, :locals => {:name => 'Mr. Ed'}
  end
  ```
9. What's the purpose of ERB?
 - ERB templates allow us to embed Ruby code within an HTML file and make dynamic changes.
10. Why do I need a development AND test database?
 - The test database is needed to sandbox dummy data that needs to be entered into a database in order to carry out testing. Development should be more representative of what data will be present in production.
11. What's responsive design?
 - "Responsive Design" refers to designing webpages/websites so that the display of content is sensitive to the device you are viewing the content on. In other words, the display will be different whether you access the site on a phone or a desktop.
12. What is CRUD and why is it important?
 - CRUD stands for Create, Read, Update, Destroy/Delete and describes the fundamental actions you can perform on a database.
13. What does HTTP stand for? 
 - HyperText Transfer Protocol.
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
 - <%= ruby_code %> Prints to the browser and returns a value.
 - <% ruby_code %> Is evaluated but does not display in the browser.
15. What's an ORM?
 - Object-relational Mapping tool. Used to interact with a database by wrapping raw SQL queries in another programming language.
16. What's the most commonly used ORM?
 -  ActiveRecord (in Ruby)
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
 - See all restaurants | GET | "/restaurants"
 - See one restaurant | GET | "restaurants/:id"
 - See form to enter new restaurant | GET | "/restaurants/new"
 - Submit form to save new restaurant | POST | "/restaurants"
 - See form to edit existing restaurant info | GET | "/restaurants/:id/edit"
 - Submit form to update a restaurant | PUT/PATCH | "/restaurants/:id" 
 - Delete a restaurant | DELETE |  "/restaurants/:id" 
18. What's a migration? 
 - ActiveRecrod migrations allow you to create and modify database schema
19. When you create a migration, does it automatically modify your database?
 - No. You have to run the migration using a rake command (rake db:migrate)
20. How does a model relate to a database?
 - The model relates to a table in the database, and the relation of its tables to other tables.
21. What's the difference between agile workflow and waterfall method?
 - Agile is an iterative approach in which a product is developed, tested, and released to production in small steps that build upon one another. The waterfall approach involves moving through development, testing, and release of the entire project in a linear fashion where each stage of the project cannot be started until the one before it has been completed.
22. What is the difference between `#new` and `#create`?
 - `#new` creates a new instance but does NOT save it to the database (need to call `#save` after)
 - `#create` creates a new instance and saves it to the database in one statement
