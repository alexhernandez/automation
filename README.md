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

## Laravel: Bootstrap Front-End
Update your `~/.bash_profile` with the following:

```bash
  alias laravel-bootstrap=~/path/to/script/laravel-bootstrap
```

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
