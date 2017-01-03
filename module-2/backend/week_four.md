## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
 - A cookie is a way of identifying a particular user.
* What’s the difference between a session and a cookie?
 - A session is an encrypted cookie.
* What’s a flash and when do you want to use flashes?
 - A flash is a message used to give the user feedback on actions taken on the site. For example, a flash could be used to let a user know that a delete action was successful, or that the login password they used was incorrect.
* Why do people say “HTTP is stateless”?
 - HTTP is stateless in that it does not "remember" or have records of your previous requests.
* What’s authentication? Explain.
 - Authentication is used to confirm a user is who they say they are.
* What’s the difference between authentication and authorization?
 - Authentication is used for identification, Authorization is used to determine what/where a user has access to on the site.
* What’s a before filter?
 - A before filter calls a method _before_ any CRUD operations take place in that controller.
* How do we keep track of a user once they’ve logged in?
 - We store their info in a cookie/session.
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
 - Namespacing is useful for creating custom uri patterns. Nesting resources makes sense to structurally represent relations between resources. For example, if a job belongs to a company, then it makes sense to nest jobs under companies. Namespacing does not represent relations in the same way.
* At a high level, what tools can you use to implement authorization? How would you use them?
 - We can use the bcrypt gem, add has_secure_password to our user model, and add password_digest as a column in our database.
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
 - An enum is declared in a model, and allows us to store attribute values as integers within the database, but query them by name.
* What are some strategies you can use to keep your views DRY?
 - Use partials, move logic to POROs, create helper methods.
