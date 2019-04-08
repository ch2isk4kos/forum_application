1. $ rails new forum

2. $ rails generate model Message title:string description:text

3. $ rake routes

4. $ rake db:migrate

5. $ rails generate controller Messages

6. add simple_form && bootstrap-sass to Gemfile

7. $ bundle install

8. restart the server

9. configure bootstrap-sass
    - app/assets/stylesheets/application.css.scss
        @import "bootstrap-sprockets";
        @import "bootstrap";
    - app/assets/javaScripts/application.js
        //= require bootstrap-sprockets

10. configure simple_form
    - $ rails generate simple_form:install --bootstrap

11. set up index, new and create actions in messages_controller.rb

12. set up views/messages/index.html.erb page

13. set up show action and show view file

14. set up update, edit and destroy actions in messages_controller.rb

15. add edit view file

16. add devise to Gemfile to add User model to application

17. $ bundle install

18. restart server

19. configure devise
    - $ rails generate devise:install
    - add to config/environments/development.rb:
       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }
    - add to app/views/layouts/application.html.erb
        ```html
            <p class="notice"><%= notice %></p>
            <p class="alert"><%= alert %></p>
            <%= yield %>
        ```    
    - $ rails g devise:views
    - $ rails generate devise User
    - $ rake routes
    - $ rake db:migrate
    - restart server

20. configure navigation functionality in
    - added bootstrap navbar to app/views/layouts/application.html.erb

21. create Associations between user and message
    - $ rails generate migration add_user_id_to_messages user_id:integer
    - $ rake db:migrate
    - update new and create message actions in messages_controller.rb

22. $ rails generate model Comment content:text message:references user:references

23. $ rake db:migrate

24. $ rails generate controller Comments

25. add _comment && _form __ partials to views/comments

26. render _comment && _form __ message show page
