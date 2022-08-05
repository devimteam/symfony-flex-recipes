Полная документаци по спецификации рецептов: [flex recipes](https://symfony.com/doc/current/setup/flex_private_recipes.html)

## Установка

Добавить endpoint в composer.json секция `extra.symfony.endpoint`

Пример:
```json
"extra": {
    "symfony": {
      "endpoint": [
        "https://api.github.com/repos/devimteam/symfony-flex-recipes/contents/index.json",
        "flex://defaults"
      ]
    }
  },
```

## Получение случайной `"ref"` значения

При добавлении или обновлении рецепта, необходимо указывать случайно сгенерированное `"ref"` значение. Что бы его получить, используй следующий PHP скрипт 
```php
php -r 'echo bin2hex(random_bytes(20));'
```