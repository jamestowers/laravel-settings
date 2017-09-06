# Lumen Settings

## This is a fork of anlutro/laravel-settings to make it work with Lumen

See https://github.com/anlutro/laravel-settings for more info on the original package

Persistent, application-wide settings for Lumen.

## Installation

1. Add `"anlutro/l4-settings": "dev-master"` to your composer file
2. Reference this VCS in the repositories section:
```
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/jamestowers/lumen-settings"
        }
    ],
```
3. Add `$app->register('anlutro\LaravelSettings\ServiceProvider');` to `bootstrap/app.php`.
4. Copy `lumen-settings/src/config/config.php` from to `/config/settings.php`
5. Make sure `$app->withFacades();` is uncommented and add `$app->configure('settings');` in `bootstrap/app.php`

### Auto-saving

Unlike the Laravel package, this fork doesnt auto-save, mainly because i'm too lazy to try.
You will need to do `Setting::save();` after setting a setting with `Setting::set('foo', 'bar');`


## More info
For more info see the original package: https://github.com/anlutro/laravel-settings


## Contact

Open an issue on GitHub if you have any problems or suggestions.


## License

The contents of this repository is released under the [MIT license](http://opensource.org/licenses/MIT).
