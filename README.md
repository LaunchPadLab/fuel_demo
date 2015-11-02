Fuel Demo
===

This is a demo of [Fuel] (github.com/launchpadlab/fuel)
Heroku example: http://fuel-demo.herokuapp.com

Setup
---

```
git clone https://github.com/LaunchPadLab/fuel_demo.git
cd fuel_demo
bundle
bundle exec rake db:create db:migrate fuel:seed
```

Now add your S3 ENV variables to application.yml (this is important as the editor needs a place to store your images):

```yml
AWS_ACCESS_KEY: YOUR-S3-ACCESS-KEY
AWS_SECRET_ACCESS_KEY: YOUR-S3-SECRET

development:
  AWS_BUCKET: your-bucket-dev
production:
  AWS_BUCKET: your-bucket
```

Then run `rails s` and navigate to localhost:3000/blog/admin

Username: admin
Password: password

You can modify those credentials in config/initializers/fuel.rb


