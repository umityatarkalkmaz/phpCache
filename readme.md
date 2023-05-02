# Basic cache data class
Converts data to json format and saves it to a file
## Dependence
This class using my string helper class. [My string helper class](https://github.com/umityatarkalkmaz/phpStringHelper) is here.
```php
Cache::get('videos');
```
`get($key)` Get data to file.
```php
Cache::put('videos',['videoname','21:20:10','creator'=>'Very Good People'],false);
```
`put($key, $data = [], $ttl = 3600)` Put data to json file and set optimally timeout.

Usage Example
```php
require 'cache.php';
use UmitYatarkalkmaz\Cache;
$videos = Cache::get('videos');
$data = ['videoname','21:20:10','creator'=>'Very Good People']
$putFile = Cache::put('videos',$data,false);
if($putFile){
    echo 'cached data';
}else{
    echo 'Failed cache data';
}
```
