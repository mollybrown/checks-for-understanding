## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
 - `rails new project_name --optional --flags`  
2. What do Models generally inherit from in rails?
 - The ApplicationRecord inhrets from ActiveRecord::Base, other models generally inheret from ApplicationRecord.
3. What do Controllers generally inherit from in a rails project?
 - The ApplicationController inherets from ActionController::Base, other controllrers generally inheret from ApplicationController. 
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
 - In config/routes.rb:
 ```
 resources :horses, only: [:show]
 ```

5. What rake task is useful when looking at routes, and what information does it give you?
 - `rake routes`, which gives you all available route prefixes, HTTP verbs, URIs, and the corrsponding controller actions currently available in your app.
6. What is an example of a route helper? When would you use them?
 - new_horse_path (prefix_path) is a route helper which can be used to find the path '/horses/new' without hard-coding the actual path.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
 - `url` returns the full url (including the HTTP protocol and domain). In other words, `url` returns an absolute path, while `_path` returns a path relative to the root of the site.
8. What are strong params and why are the necessary?
 - strong params prevent users from passing unwanted input params to the controller. Good for preventing hacking.
9. What role does `form_for` play in helping us create our forms?
 - `form_for` is a rails helper that generates an HTML form for a given object passed to it.
10. How does `form_for` know where to submit the user's input?
 - when you pass form_for an object, it checks to see if that object already exists. If it already exists, the input is submitted to the edit route. If not, it is submitted to the new route so that the object can then be created.
11. Create a form using a `form_for` helper to create a new `Horse`. 

```
<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>

  <%= f.label :breed %>
  <%= f.text_field :breed %>

  <%= f.submit %>
  <% end %>
  ```
  
12. Why do we want to validate our models?
 - In validating our models we can check that all the necessary attributes/columns/fields are present (and/or unique and/or probably other things that we have not learned yet) to create an object. This helps ensure that our objects in the database are well-formed. 
