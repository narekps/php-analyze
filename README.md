# php-analyze
Тут собраны самые популярные статические анализаторы для PHP кода.

### Установка
```bash
composer require --dev narekps/php-analyze
```

### Примеры запуска анализатора

- **cbf** - Code Beautifier and Fixer
```bash
vendor/bin/phpcbf --standard=./vendor/narekps/php-analyze/phpcs.xml -s -p --colors --extensions=php --encoding=utf-8 --tab-width=4 --no-cache --parallel=100 ./src
```

- **cs** - Code Sniffer
```bash
vendor/bin/phpcs --standard=./vendor/narekps/php-analyze/phpcs.xml -s -p --colors --extensions=php --encoding=utf-8 --tab-width=4 --no-cache --parallel=100 ./src
```

- **phpstan**
```bash
vendor/bin/phpstan analyze -c ./vendor/narekps/php-analyze/phpstan.neon ./src
```

- **psalm**
```bash
vendor/bin/psalm -c=./vendor/narekps/php-analyze/psalm.xml --show-info=false --threads=4 ./src
```

- **phan**
```bash
vendor/bin/phan --config-file=./vendor/narekps/php-analyze/phan.php --processes=4 --progress-bar --directory=./src --directory=./vendor
```

*В примерах используется директория ./src для анализа.
Можно укзать несколько директорий разделяя пробелом.*