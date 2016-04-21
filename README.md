Yii2 Mailgun Mailer
===================
Mailgun mailer for Yii 2 framework.

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist e96/yii2-mailgun-mailer "*"
```

or add

```
"e96/yii2-mailgun-mailer": "*"
```

to the require section of your `composer.json` file.


Usage
-----

First, update your mailer config like so:

```php
'mailer' => [
  'class' => 'e96\mailgunmailer\Mailer',
  'domain' => 'domain.com',
  'key' => 'api-key',
  'tags' => ['yii'],
  'enableTracking' => false, //or true
],
```

Yii's mailer will now use the Mailgun configuration, so send mail like normal:

```php
<?php
Yii::$app->mailer->compose('<view_name>', <option>)
->setFrom("<from email>")
->setTo("<to email>")
->setSubject("<subject>")
// ->setHtmlBody("<b> Hello User </b>")
// ->setTextBody("Hello User")
->send();
?>```
