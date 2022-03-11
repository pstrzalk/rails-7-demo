# README

Rails 7 demo application, as presented by DHH at https://www.youtube.com/watch?v=mpWFrUwAN88

List of commands:
```sh
npm install rails
rails new rails-7-demo
cd rails-7-demo

rails generate scaffold post title:string content:text
rails db:migrate -- sqlite, creates a DB as well

rails action_text:install
bundle
rails db:migrate

./bin/importmap pin local-time --download
# assets:clear to make sure all is updated

rails g resource comment post:references content:text

rails g mailer comments submitted
# preview of this mailer http://localhost:3000/rails/mailers/comments_mailer/submitted

# comments are saved via POST but broadcasted via websockets
# comments may be created / updated / destroyed and all that gets broadcasted

rails test

rails db:system:change --to=postgresql
```
