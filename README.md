# PHPStorm Live Templates for Drupal 7 and Drupal 8

## What ? Why ?

Lazy programmers (i.e. every programmer) like to use code snippets. The goal is
to write less code and program faster. IDE's (or text editors like VIM) allow
the use of such snippets to write for us commonly used functions.

The purpose of these Live Templates is to provide Drupal devs such templates
for Drupal hooks. It was generated using a Perl script that basically create
PHPStorm Live Templates from *.api.php files in Drupal /includes and /modules
directories. The output is a bit raw, so it needs some love and polish.

## Quick and easy install

1. Download and copy the *xml* file(s) from this repo to your templates folder:

* Windows: `<your home directory>\.<product name><version number>\config\templates`
* Linux: `~\.<product name><version number>\config\templates`
* OS X: `~/Library/Preferences/<product name><version number>/templates`

e.g. `~/Library/Preferences/PhpStorm2016.2/templates` on OS X for PhpStorm 2016

2. Restart PhpStorm.

3. To see all templates, go to *Preferences->Live Templates* and expand the Template Group.

## How to use

While editing, use `CMD + J` (osX) or `CTRL + J` to start inserting a live template. 
Type `h_HOOKNAME<tab>` for short version, `hook_HOOKNAME<tab>` for annoted version (with core comments).

The hook should be completed as you would see in the api docs.


## How to use the script generator (optional)

The script generator allows you to create live templates by scanning the `.api.php` files that exist in your drupal project. It looks for functions starting with `function hook_` and uses that to build the live templates. 

You need Perl in your machine. This script was written under Debian Linux, so it may need some adaptations for others OS's.

Type these commands :

    $ cd /path/to/drupal  
    $ find . -name \*.php | xargs grep -l '^function hook_' | xargs /path/to/parse_drupal_api.pl > ~/.WebIde10/config/templates/user.xml


## License

Copyright (C) 2011  Jeremie Le Hen <jeremie@le-hen.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

## Credits

Props to Jeremie Le Hen who wrote the Perl script that generated the templates.  
Special thanks to [blup](https://github.com/blup/snippets) for the original idea and work (VIM snippets for Drupal)

Drupal 8 templates added by Jeremy Graham
