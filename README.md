yii-less-extension
==================

Yii Less Extension gives a _VERY_ simple and straight forward way to include LESS files in your Yii view files. Yii Less Extension adds a method to the `CClientScript` class, namely `registerLessFile` which is very similary to the `registerCssFile` method, to directly link LESS files in your Yii view files.

##Requirements

Requires Yii 1.1 or above.

##Usage
* Download and extract the extension package to `protected/extensions` directory of your application.
* Make the following modifications to your `protected/config/main.php` under the components section of the config:
~~~
<?php 
array(
  // .....
  'components'=>array(
    // .....
    'clientScript' => array(
      'class' => 'ext.yiiless.components.YiiLessCClientScript',
    ),
    // .....
  ),
  // .....
),
?>
~~~

* In any of your view files just include your less file using `Yii::app()->clientScript->registerLessFile("full-or-relative-path-to-your-less-file/style.less");`

Eg: 
~~~
<?php Yii::app()->clientScript->registerLessFile(Yii::getPathOfAlias("less-files/site.less"); ?>
~~~
Adding the above in your `layouts/main.php` will render `<web-application-root>/less-files/site.less` file as `site.css` delivered from your assets.

##Resources

 * [LESS CSS](http://lesscss.org/)
 * [LESS for PHP](http://leafo.net/lessphp/)

