# Session 1 Notes

## Session Overview

* Installation / Configuration
  * Windows, Mac OS X, Linux, RVM
* Tools Overview
  * ruby, rails, gem, bundler, git
  * Editors and IDEs
* Your first Ruby on Rails application
  * Creating and Viewing the App
  * Ruby on Rails Philosophy
  * Ruby on Rails Architecture
  * Model - View - Controller
  * Application directory structure
* Homework
  * Learn Some Ruby
  * Join The Community
  * Sign Up For GitHub
  * Sign Up For Heroku

## Installation

### Windows

Use the RailsInstaller

* http://railsinstaller.org/

### Mac OS X

Ruby Versions Included:

* Tiger (10.4) 1.8.2
* Leopard (10.5) 1.8.6
* Snow Leopard (10.6) 1.8.7

You will need Xcode - Install from your Mac OS X DVD or
download from http://developer.apple.com/xcode/

### Linux

Ubuntu Ruby Versions Included:

* dapper (6.06LTS) 1.8.4
* hardy (8.04LTS) 1.8.6
* lucid (10.04LTS) 1.8.7
* maverick (10.10) 1.8.7
* natty (11.04) 1.8.7

Debian Ruby Versions Included:

* stable 1.8.7
* testing 1.8.7
* unstable 1.8.7

CentOS Ruby Versions Included:

* CentOS 5 1.8.5

#### Installing on Ubuntu:

    sudo apt-get install git ruby rubygems1.8
    sudo gem install rails
    gedit ~/.bashrc
    Add this line at the bottom:
    PATH="/var/lib/gems/1.8/bin:$PATH"

### RVM

Ruby Version Manager

https://rvm.beginrescueend.com/

## Ruby Learning Resources

### New to programming

Learn to Program by Chris Pine
http://pine.fm/LearnToProgram/

Free online version in HTML

### New to Ruby

Beginning Ruby by Peter Cooper
http://www.rubyinside.com/why-the-lucky-stiffs-delightful-foreword-for-beginning-ruby-4550.html

Peter Cooper shared this link to the PDF version of his book
http://no.gd/begruby2.pdf

Ruby in Twenty Minutes
http://www.ruby-lang.org/en/documentation/quickstart/

Try Ruby - online interactive tutorial
http://tryruby.org/

Mr. Neighborly's Humble Little Ruby Book
http://www.humblelittlerubybook.com/book/html/index.html

### New to Ruby (and a little crazy)

Why's Poignant Guide to Ruby
http://mislav.uniqpath.com/poignant-guide/

### Test your knowledge

Ruby Koans
http://rubykoans.com/

Ruby Quiz
http://rubyquiz.com/


## Git Learning Resources

Pro Git

Free online book, also in print

http://progit.org/book/

GitHub Bootcamp

http://help.github.com/

Git Reference

http://gitref.org/

Git Community Book

http://book.git-scm.com/


## Rails Hosting

Heroku

* They offer a free plan
* Simple deployment with git
* http://www.heroku.com/

Rackspace Cloud Servers

* 1.5 cents per hour for your own server
* http://www.rackspace.com/cloud/


## Local Community Resources

Austin on Rails

* Meets 4th Tuesdays, 7-9 PM
* http://austinonrails.org/

Austin.rb

* Meets 3rd Thursdays, 7-9 PM
* http://austinrb.org/

Lone Star Ruby Conference

* August 11-13, 2011
* http://www.lonestarrubyconf.com/


## Building and Deploying the Class Roll App

    rails new classroll
    cd classroll

    bundle install

    rake db:create

    git init
    git add .
    git commit -m "Initial commit"

    rails generate scaffold Student name:string email:string url:string bio:text

    rake db:migrate

    git add .
    git commit -m "Adding students"

    git rm public/index.html
    Edit config/routes.rb

    git add .
    git commit -m "Updating routes"

    git mv public/stylesheets/scaffold.css public/stylesheets/styles.css
    git commit -m "Renaming stylesheet"

    Edit app/views/layouts/application.html.erb
    Edit app/views/students/_form.html.erb
    Edit app/views/students/index.html.erb
    Edit app/views/students/new.html.erb
    Edit app/views/students/show.html.erb
    Edit public/stylesheets/styles.css

    git add .
    git commit -m "Updating views"

    Edit app/models/student.rb

    git add .
    git commit -m "Adding validation"

    git remote add origin git@github.com:anthonylewis/classroll.git
    git push -u origin master

    heroku create
    heroku keys:add
    git push heroku master
    heroku rake db:migrate


