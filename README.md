# META+Automation
Hassle Free Setup of Your Mac Binaries, Applications, Projects and Plugins.

## Getting Started

*  Clone the repo URI `git clone https://github.com/csun-metalab/automation.git`
*  Create an alias for the desired script in your `~/.bash_profile`

```bash
  # Add to your .bash_profile
  alias laravel-bootstrap=~/path/to/script/laravel-bootstrap
```
* Restart OR source your command-line with `source ~/.bash_profile`
* Run the script with `laravel-bootstrap`

Thats A Wrap!

## Adding Dependencies

Before you get started you may need to add the following:

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

Thats A Wrap!
