# Anythink Market Backend

The Anythink Market backend is Ruby web app written with [Ruby On Rails](https://rubyonrails.org/)

## Getting started
1. Select the correct Ruby version: `rvm use 2.7.0`
2. Create a new gem set: `rvm gemset create anythink-market` && `rvm gemset use anythink-market`
3. Install all dependencies: `bundle install`
4. Set a cool name for your DB in `database.yml` or keep the example one `anythink_d`.
5. Run `rails db:create` and you will have your own local DB
6. Run `rails db:migration` to create all schema tables.
 

To start the app use: `./start.sh` from the backend directory.

Make sure your DB is up and running.

#Troubleshooting
- You may have problems installing `pg` from the Gemfile.
  You can find it installing posgresql on your local pc (For macOS: `brew install postgresql`), or use Docker for this step.
  After that, you can run again `bundle install`

- Both apps are using the default port, so check you don't have anything listening on that part already

## Dependencies

- [acts_as_follower](https://github.com/tcocca/acts_as_follower) - For implementing followers/following
- [acts_as_taggable](https://github.com/mbleigh/acts-as-taggable-on) - For implementing tagging functionality
- [Devise](https://github.com/plataformatec/devise) - For implementing authentication
- [Jbuilder](https://github.com/rails/jbuilder) - Default JSON rendering gem that ships with Rails, used for making reusable templates for JSON output.
- [JWT](https://github.com/jwt/ruby-jwt) - For generating and validating JWTs for authentication

## Folders

- `app/models` - Contains the database models for the application where we can define methods, validations, queries, and relations to other models.
- `app/views` - Contains templates for generating the JSON output for the API
- `app/controllers` - Contains the controllers where requests are routed to their actions, where we find and manipulate our models and return them for the views to render.
- `config` - Contains configuration files for our Rails application and for our database, along with an `initializers` folder for scripts that get run on boot.
- `db` - Contains the migrations needed to create our database schema.