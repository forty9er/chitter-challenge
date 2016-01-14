[![Build Status](https://travis-ci.org/forty9er/chitter..svg)](https://travis-ci.org/forty9er/chitter.)

# @Chitter.

### Duration

2 days


### Live demo

https://cryptic-citadel-4502.herokuapp.com/


### Installation

Download the files in the repo, install the required Gems and run via a Sinatra server via Rackup on your local machine. You will also need a working PostgreSQL installation (you can install this via Brew).
The main controller is 'app.rb' in the 'app' directory. You will need a Ruby interpreter (if you are running OS X you already have this) and RVM installed.

To clone the repo on your machine:

```
$ git clone https://github.com/forty9er/chitter_challenge
```

Then from the root folder, install the Gems, create and initialise the database and finally run the app:
```
$ bundle
$ createdb chitter_development
$ rake db:auto_migrate RACK_ENV=development
$ rackup app/config.ru
```

Now navigate to http://localhost:9292/ in your browser.


### Usage

You can view 'Peeps' simply by navigating to the website, or by clicking on the "@Chitter" logo.

![Main Peep Feed](https://www.dropbox.com/s/m9pmcm94ssdckeo/CHITTER_1.png?raw=1)

In order to 'Peep' you need to create an account and log in. 

![Sign up](https://www.dropbox.com/s/1l1l5hj9a2umjc4/CHITTER_2.png?raw=1)

You can then hit the Peep! button and submit your Peep.

![Peep](https://www.dropbox.com/s/snudd7s4camv1m8/CHITTER_3.png?raw=1)

Once you are finished 'Peeping' you can log out using the 'Log out' button.

![Feed and log out](https://www.dropbox.com/s/sd3d945xdu25dcm/CHITTER_4.png?raw=1)


### Testing

The app was built using TDD. Before running you will need to initialize the test database:

```
rake db:auto_migrate RACK_ENV=test
```

RSpec tests can be run from the root directory simply by running:

```
rspec
```


### TODO

* Responsive (Bootstrap) styling (larger buttons, position elements, logo and backdrop.)
* Consider using partials.
* Consider whether controllers can be slimmed down further.
* Use view helpers to remove amount of embedded Ruby and comply with SRP.
* Correct semantics for HTML form markup.
* Use article etc. not div in HTML.
* Integrate tagging other users to create conversations.
* Rake task for first DB setup.
* More comprehensive feature testing.


### Technologies used

* Ruby
* PostgreSQL
* DataMapper
* HTML
* CSS
* TDD (via Rspec & Capybara)
* Sinatra
* Heroku
* Rake

### Original challenge instructions
[via the power of Git](https://github.com/forty9er/chitter-challenge/blob/5ab36f4a528f7985d7071bbc8fccb852afe3e9b9/README.md)