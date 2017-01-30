## Week One - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What is `json` and why is it important?
 - JSON stands for JavaScript Object Notation. It is a data format that stores information in key-value pairs. It balances being both machine and human readable. It is important because it is a standard way of formatting and transferring data as of today.
2. What's the difference between `joins` and `includes` in ActiveRecord? 
 - `includes` loads ALL attributes from the tables you join (eager loading), while `joins` only loads the attributes you select within your query (lazy loading).
3. What's an API?
 - API stands for Application Program Interface. APIs are used to expose an app's data externally.
4. How do we test an internal API (in general)?
 - With controller tests (testing routing/API endpoints)
5. What are two different ways to customize your `json`?
 - 1) Use Active Model Serializers to filter which attributes are exposed at each endpoint, 2) use ERB templates to control which parts of the JSON response are displayed to the user on screen.
