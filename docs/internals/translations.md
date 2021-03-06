Translation workflow
====================

Yii is translated in many languages in order to be useful for international applications and developers. Two main areas
where contribution is very welcome are documentation and framework messages.

Framework messages
------------------

Framework has two types of messsages: exceptions that are intended to developer and are never translated and messages
that are actually visible to end user such as validation errors.

In order to start with message translation:

1. Check `framework/yii/messages/config.php` and make sure your language is listed in `languages`.
2. Go to `framework/yii` and run `yii message/extract messages/config.php`.
3. Translate messages in `framework/yii/messages/your_language/yii.php`. Make sure file is saved using UTF-8 encoding.
4. Make a pull request.

In order to keep your translation up to date you may run `yii message/extract messages/config.php` again. It will
automatically re-extract messages keeping unchanged ones intact.

In the translation file each array element represents the translation (value) of a message (key). If the value is empty,
the message is considered as not translated. Messages that no longer need translation will have their translations
enclosed between a pair of '@@' marks. Message string can be used with plural forms format. Check [i18n section
of the guide](i18n.md) for details.
