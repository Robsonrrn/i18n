## php-i18n

#### Installation
	
	$ composer require robsonrrn/php-i18n

#### Configuration

Create your yml locale files inside some folder in your project. See the yml file example:

```yaml
pt-BR:
  hello: Olá I18n
  user:
    name: Nome do usuário
  errors:
    messages:
      unauthorized: Não autorizado

```

> You can use multiple languages and multiple files for each language, ex:
> - pt-BR.yml
> - models.pt-BR.yml
> - errors.pt-BR.yml
> - en.yml
> - models.en.yml
> - errors.en.yml


Say to the plugin where this files were placed

```php
\Robsonrrn\I18n::instance()->addLocalesPath(__DIR__ . '/config/locales')->setCurrentLocale('pt-BR');
```

#### Usage 

```php
Robsonrrn\I18n::instance()->hum('hello');
```

