## IG Monitoring

![zrzut ekranu 2018-02-10 o 17 19 33](https://user-images.githubusercontent.com/839118/36064169-1e37d942-0e87-11e8-8c05-b7ac197af709.png)
![zrzut ekranu 2018-02-10 o 17 20 50](https://user-images.githubusercontent.com/839118/36064168-1e1cd700-0e87-11e8-853c-b7a86311b6bf.png)
![zrzut ekranu 2018-02-10 o 17 21 54](https://user-images.githubusercontent.com/839118/36064167-1e013950-0e87-11e8-8da7-48943127c58c.png)

# Version
Early dev stage.  **Use at your own risk.**

# Install
- git clone
- composer install

# Config
- create database: mysql, utf8mb4
- copy config/db.dist => config/db.php
- register google project for Google Sign-In
- copy config/authClientCollection.php.dist => config/authClientCollection.php
- [configure worker](https://github.com/yiisoft/yii2-queue/blob/master/docs/guide/worker.md)
- create cron hourly for: `./yii stats/update-accounts` and `./yii stats/update-tags`

# Manual
Everything should be added from the command line.

- `./yii proxy/create`
- `./yii monitoring/account`
- `./yii monitoring/tag`
- `./yii help monitoring/account` - displays help for the command

See `./yii` for more commands.


# Limitations
- You need at least one, **WORKING proxy** for accounts and one for tags.
- php >= 7.1
- mysql >= 5.5

# Legal
This code is in no way affiliated with, authorized, maintained, sponsored or endorsed by Instagram or any of its affiliates or subsidiaries.
This is an independent tool. **Use at your own risk.**

