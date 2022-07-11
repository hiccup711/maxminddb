1. 安装 php 扩展
    ```php
    atp install libmaxminddb 
    pecl install maxminddb
    ```
2. 安装扩展包
    ```php
    composer require maxmind-db/reader
    ```
3. 使用
    ```php
    $reader = new Reader('/Users/Ricky/Sites/GeoLite2-Country.mmdb'); // 数据库文件
    $ip = '161.81.198.57'; // 自己获取 ip 地址
    
    var_dump($reader->get($ip));
    ```