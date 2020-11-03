# 99 Bottles

(Thanks to the [North West Ruby Group website](https://nwrug.org/quizzes/99-bottles-of-oo-programming) for the information on setting this up)

## Prerequisites

You will need Ruby 1.9 or above installed on your machine. Check which version you have with the following command:

    ruby --version

If you don't have a new enough version of Ruby, follow the instructions on ruby-lang.org to install it.

You will also need the Minitest testing library version 5 or above. You can check which version you have with the following command:

    gem list minitest

If you don't have Minitest version 5 or above, install it with the following command:

```gem install minitest --version "~> 5.9"```

## Getting the exercise

There is a repository on Github that will help you get set up:

    git clone --depth=1 --branch=exercise https://github.com/sandimetz/99bottles.git

The directory structure should look like this:

    ├── lib
    │   └── bottles.rb
    └── test
        └── bottles_test.rb
        
## Doing the exercise

The test suite can be run by running the following command from the project directory:

    ruby test/bottles_test.rb
    
The test suite contains one failing test and many skipped tests. Your goal is to write code that passes all of the tests. Compete the exercise by following these steps:

- run the tests and note the failure
- write only enough code to pass the failing test
- unskip the next test

Repeat the steps until no tests are skipped and you've written code to pass them all.


## Installing Ruby

### Windows

There's an installer, it's easy.
http://rubyinstaller.org/

### Mac

Newer macs ship with a usable version of Ruby.

Try `ruby -v` in a terminal window, and if it's 1.9.x or 2.x you're fine.

http://www.railstutorial.org/book/beginning#sec-install_ruby
http://tutorials.jumpstartlab.com/topics/environment/environment.html
http://docs.railsbridge.org/installfest/macintosh

### Linux

Ubuntu: http://docs.railsbridge.org/installfest/linux
https://www.ruby-lang.org/en/installation/
