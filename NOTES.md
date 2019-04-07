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
