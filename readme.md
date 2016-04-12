# Background

# Setup

```
git clone git@github.com:timbroder/mock-bootable-laravel-model-trait.git
cd mock-bootable-laravel-model-trait
```

# Test

To see the trait working in the app:

```
artisan testtrait
```
Expected output:

```
Testing that class: App\MyModel has method: bootMyTrait because of Trait: App\MyTrait
Class: App\MyModel has method: bootMyTrait
Booting MyTrait
```

To see mock failing:

```
phpunit
```
Unexpected output:

```
PHPUnit 5.1.0 by Sebastian Bergmann and contributors.

E                                                                   1 / 1 (100%)
Testing that class: Mock_MyModel_9ee820db has method: bootMyTrait because of Trait: App\MyTrait
Class: Mock_MyModel_9ee820db has method: bootMyTrait
Class: Mock_MyModel_9ee820db failed calling bootMyTrait


Time: 129 ms, Memory: 18.00Mb

There was 1 error:

1) ExampleTest::testTraitBooting
PHPUnit_Framework_MockObject_BadMethodCallException:

mock-bootable-laravel-model-trait/vendor/laravel/framework/src/Illuminate/Database/Eloquent/Model.php:326
mock-bootable-laravel-model-trait/vendor/laravel/framework/src/Illuminate/Database/Eloquent/Model.php:309
mock-bootable-laravel-model-trait/vendor/laravel/framework/src/Illuminate/Database/Eloquent/Model.php:296
mock-bootable-laravel-model-trait/vendor/laravel/framework/src/Illuminate/Database/Eloquent/Model.php:277
mock-bootable-laravel-model-trait/tests/ExampleTest.php:16
```