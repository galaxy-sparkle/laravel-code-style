# PHP CS Fixer - Laravel Coding Style Ruleset

基于 [Laravel Shift](https://gist.github.com/laravel-shift/cab527923ed2a109dda047b97d53c200) 和 [StyleCI Laravel Preset](https://docs.styleci.io/presets#laravel)

基于 Laravel 8.35.1 版本对 framework 目录进行测试 只有两个文件格式化有冲突:
1. `vendor/laravel/framework/src/Illuminate/Cache/PhpRedisLock.php`

从 {@inheritDoc} => {@inheritdoc} 属于该文件本身的问题 其他框架文件都是 {@inheritdoc}

2.  `vendor/laravel/framework/src/Illuminate/View/Concerns/ManagesComponents.php`

```php
# 从  (------------ 为空格)
$this->slots[$this->currentComponent()]
------------[$currentSlot] = new HtmlString(trim(ob_get_clean()));
# 格式化为
$this->slots[$this->currentComponent()][$currentSlot] = new HtmlString(trim(ob_get_clean()));
```
