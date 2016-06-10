# PHP Symfony tests

Test tools configuration template for Symfony projects.

Run all your tests and static code analysis tools in just one command.
Included tools are phpunit, phpcs, phploc, phpcpd, phpmd.


## Requirements

- You need to have **composer** installed globally
- **xdebug** extension should be enabled
- You may have **phing** installed globally instead of using the dependency


## Setup

- Add the following packages int your ```composer.json``` :
```json
    "require-dev": {
        "phing/phing": "^2.14",
        "phpunit/phpunit": "^5.4",
        "phpmd/phpmd": "^2.4",
        "phploc/phploc": "^3.0",
        "sebastian/phpcpd": "^2.0",
        "squizlabs/php_codesniffer": "^2.6"
    }
```

- Copy all the content of the */files* directory at the root of your project
- Run
```bash
    $ composer install
```

That's it, you're now ready to launch static code analysis tools, and unit tests


## Usage

If you don't have phing installed globally:
```bash
    $ alias phing=vendor/bin/phing
```

Launch all unit tests + static code analysis
```bash
    $ phing
```

Launch unit tests only
```bash
    $ phing unit
```

List available tasks:
```bash
    $ phing -l
```


## TODO

- Add docker integration to run tests in containers
- Add behavioual tests


## License

WTFPL v2

![WTFPL v2](http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-1.png)

See the LICENSE file.


