# Ruby on Rails Tutorial sample application

This is the sample application for
[*Ruby on Rails Tutorial:
Learn Web Development with Rails*](http://www.railstutorial.org/)
by [Michael Hartl](http://www.michaelhartl.com/).

## License

All source code in the [Ruby on Rails Tutorial](http://railstutorial.org/)
is available jointly under the MIT License and the Beerware License. See
[LICENSE.md](LICENSE.md) for details.

## Getting started

To get started with the app, clone the repo and then install the needed gems:

```
$ bundle install --without production
```

Next, migrate the database:

```
$ rails db:migrate
```

Finally, run the test suite to verify that everything is working correctly:

```
$ rails test
```

If the test suite passes, you'll be ready to run the app in a local server:

```
$ rails server
```

For more information, see the
[*Ruby on Rails Tutorial* book](http://www.railstutorial.org/book).


## NOTE : Don't use sqlite3 with Heroku !!!!!! use pg (Postgres instead)

# How to reverse Rails generate
$ rails generate controller StaticPages home help
$ rails destroy  controller StaticPages home help

$ rails generate model User name:string email:string
$ rails destroy model User

Migrations change the state of the database using the command : $ rails db:migrate
We can undo a single migration step using : $ rails db:rollback
To go all the way back to the beginning, we can use :
$ rails db:migrate VERSION=0
# we can change VERSION=?? , where the version numbers come from listing the migrations sequentially.

PATCH and DELETE, are designed for updating and destroying things on the remote server

# Sometimes, Spring does not close itself
# We can kill it by
- ps aux | grep spring , kill -15 pid
- spring stop
Sometimes this doesn’t work, though, and you can kill all the processes with name spring using the pkill command as follows:
- pkill -15 -f spring
