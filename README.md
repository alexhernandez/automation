# META+Automation
Hassle Free Setup of Your Mac Binaries, Applications, Projects and Plugins.

## Table of Contents
- [Quick Start Guide](https://github.com/csun-metalab/automation#quick-start-guide)
- [Laravel: Bootstrap Front-End](https://github.com/csun-metalab/automation#laravel-bootstrap-front-end)
- [Mac Application Setup](https://github.com/csun-metalab/automation#mac-application-setup)
- [Sublime Text Plugins](https://github.com/csun-metalab/automation#sublime-text-plugins)
- [Dependencies](https://github.com/csun-metalab/automation#dependencies)

## Quick Start Guide:

1. Clone the repo URI `git clone https://github.com/csun-metalab/automation.git`
2. Create an alias with the path to desired script in `~/.bash_profile`
3. Restart OR source command-line with `source ~/.bash_profile`
4. Run the desired script (ex. `laravel-bootstrap`, `mac-setup`, or `sublime-plugins`)

## Laravel: Bootstrap Front-End and Back-End
Update your `~/.bash_profile` with the following:

```bash
  alias laravel-bootstrap=~/path/to/script/automation/laravel/laravel-bootstrap
```

The `laravel-bootstrap` script will also automatically install Bower, Gulp, and Composer for you if you do not already have those dependencies.

During the installation of the Node packages the script will prefer Yarn over NPM.

Create a new Laravel project w/ `laravel new <project-name>` followed by `laravel-bootstrap`. The following can now be automatically added to your Laravel project.

```bash
  Laravel Project
  ├── .bowerrc
  ├── bower.json
  ├── elixir.json
  ├── gulpfile.js
  ├── node_modues
  │   ├── gulp
  │   └── laravel-elixir
  ├── resources
  │   └── views
  │       ├── layouts
  │       │   ├── master.blade.php
  │       │   └── partials
  │       └── pages
  │           └── landing.blade.php
  └── vendor
      └── bower_components
```

If you do not wish to create a new Laravel project manually the `laravel-bootstrap` script can also create a project automatically if you are not currently within a Laravel project directory.

### Use Default Settings

You can execute the script with a flag in order to take the default action for all commands that would require input:

`laravel-bootstrap --use-defaults`

You will not be prompted for any input during any of the actions.

#### All Actions Performed

The default actions will be performed in order:

1. Install Bower globally if it does not exist
2. Install Gulp globally if it does not exist
3. Install Composer in /usr/local/composer if it does not exist
4. Create a fresh Laravel project if the script was not executed in a Laravel project directory
5. Create a Laravel .env file if one does not already exist
6. Create master and partial layout view templates if they do not already exist
7. Create a .bowerrc file if one does not already exist
8. Create an elixir.json file if one does not already exist
9. Create a gulpfile.js file if one does not already exist
10. Install the relevant Composer packages
  * laravelcollective/html
  * guzzlehttp/guzzle
  * tiesa/ldap
  * csun-metalab/laravel-proxypass
  * barryvdh/laravel-debugbar
11. Add the relevant service providers from the Composer packages to config/app.php
12. Add the relevant alias from the Composer packages to config/app.php
13. Publish all vendor resources from all Composer packages
14. Create a bower.json file if it does not already exist
15. Install all local Node packages from Laravel project's package.json file

## Mac Application Setup

```bash
  # Add to your .bash_profile
  alias mac-setup=~/path/to/script/mac-setup
```

## Sublime Text Plugins

```bash
  # Add to your .bash_profile
  alias sublime-plugins=~/path/to/script/sublime-plugins
```

## Dependencies

Before you get started you may also need to add the following:

```bash
  # Adding Homebrew
  $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

  # Adding Node w/ Homebrew
  $ brew install node

  # Adding Bower Globally
  $ npm install -g bower

  # Adding Gulp Globally
  $ npm install --global gulp

  # Adding Composer Globally
  $ curl -sS https://getcomposer.org/installer | php
  $ mv composer.phar /usr/local/bin/composer
```
