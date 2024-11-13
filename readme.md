## Basic example of docker setup for laravel

Your laravel app goes in a folder `app` at the same level as the present files. You must change your env or the compose file to match the database username and password
`docker compose up`
The app may be accessible at app.localhost

## To Do

- [ ] Make one setup for developement
  - [ ] Add support for Telescop
  - [ ] Make bind mounts and watchers
- [ ] And one for production
  - [ ] Add security by adding a user and set permissions
  - [ ] Make a complete setup to hold multiples laravelapplications
