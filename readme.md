# Basic example of docker setup for laravel

Your laravel app goes in a folder `app` at the same level as the present files. You must change your `.env` or the compose file to match the database username and password. The `.env` file here is an example of possible configuration.

```
docker compose up
```

The app may be accessible at app.localhost

If you plan to use Reverb, Horizon, Octane, you might want to install them in your project:

```
php artisan install:broadcasting
```

```
composer require laravel/horizon --ignore-platform-reqs
php artisan horizon:install
```

```
composer require laravel/octane
php artisan octane:install
```

The `--ignore-platform-reqs` is important if you're on Windows because horizon can't run on windows.

If you have trouble with `cors(Cross-Origin Request Blocked)` with inertia and https in local development, add `$middleware->trustProxies(at: '*')` in `/bootstrap/app`;

## To Do

- [ ] Make one setup for developement
  - [ ] Add support for Telescop
  - [ ] Bind mounts and watchers (watch code changes in developpement)
- [ ] And one for production
  - [ ] Add security by adding a user and set permissions
  - [ ] Make a complete setup to hold multiples laravelapplications
  - [ ] Add support for optimizing, cache, and migrations
  - [ ] Add support for automated backups
- [ ] Add support for mails
