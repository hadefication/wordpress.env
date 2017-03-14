## Wordpress.env

Just another Wordpress with [phpdotenv](https://github.com/vlucas/phpdotenv). This ships with [Wordpress 4.7.3](https://wordpress.org/download/) so please follow it's system [requirements](https://wordpress.org/about/requirements/).

### Requirements
1. PHP 7.0 or greater
2. [Composer](https://getcomposer.org/)

### Usage
1. Clone or download this repo.
2. Run `composer install` to install the required package.
3. Copy `.env.stub` and rename it to `.env`. Update the configurations in the file now named as `.env`.
4. Or run `make setup` if you have Makefile support to run steps 1 and 2 then update the configurations in the generated `.env` file.
4. Run the installer by accessing `http://yourdevdomain.dev`. This could be your [http://localhost](http://localhost) or something else depending on your setup.
5. Cheers!

## Variables
0. `DEBUG` for debugging mode. Set `true` or `false` to toggle debugging mode. Defaults to `false`.
1. `DB_NAME` for the database name.
2. `DB_USER` for the database user.
3. `DB_PASSWORD` for the database password.
4. `DB_HOST` for the database host. This can be a hostname or an ip.
5. `DB_CHARSET` for the database character set. Defaults to **utf8** (Unicode UTF-8). See this [link](https://dev.mysql.com/doc/refman/5.6/en/charset-charsets.html) for more details on valid MySQL characters sets.
6. `DB_COLLATE` for database collation. Read [this](https://codex.wordpress.org/Editing_wp-config.php#Database_collation) for more details on database collation.
7. `DB_TABLE_PREFIX` for the database table prefix. It's important to add `_` after the prefix. Defaults to `wp_`.
8. `AUTH_KEY` `SECURE_AUTH_KEY` `LOGGED_IN_KEY` `NONCE_KEY` `AUTH_SALT` `SECURE_AUTH_SALT` `LOGGED_IN_SALT` `NONCE_SALT` are security keys. You can grab its values over [here](https://api.wordpress.org/secret-key/1.1/salt/).
9. `WP_HOME` for the default home url. Using this will save you a database query, equates to performance plus plus.
10. `WP_SITEURL` for the default site url. Using this will save you a database query, equates to performance plus plus.
11. `FS_CHMOD_FILE` to override file permissions. Defaults to `0644`.
12. `FS_CHMOD_DIR` to override directory permissions. Defaults to `0755`.
13. `WP_MEMORY_LIMIT` to override PHP's memory limit. Adjust this according to your needs specially if you have resources hungry plugins. Defaults to `64M`.
14. `WP_MAX_MEMORY_LIMIT` to override PHP's max memory limit. Adjust this according to your needs specially if you have resources hungry plugins. Defaults to `256M`.
15. `WP_ALLOW_MULTISITE` to allow multisite support. Defaults to `false`.
16. `WP_ALLOW_REPAIR` to allow database optimization and repair. Set back to `false` once the process is done. Defaults to `false`.

## Example
```
DEBUG=false

DB_NAME=db_name
DB_USER=db_user
DB_PASSWORD=QYewQFprw4s5VnPeKRR6QwS9
DB_HOST=localhost
DB_CHARSET=utf8
DB_COLLATE=

DB_TABLE_PREFIX=myprefix_

AUTH_KEY=")ssywuO+{|AtxE^Cgofr>^P&3O)Lqg+%Xf7M;);v9Vay&&^35i%DxH[FTCMYC)3{"
SECURE_AUTH_KEY=~"ngQ]Y88M[|!jh%n+/lTp@ecDwd[j|BcyA!i5p&e);REmIX?~_m*VI5>Fsr^hLAA"
LOGGED_IN_KEY="z+PjpsB%5+x=+!-WsZf0ue@VYx&S`d<Eo[4sBK&qb{:%}s9,16_6L qWNR8k-I]|"
NONCE_KEY="]tRE( {+7S=&$nBJ.NP.Se|yR<(<2TBglTPEb7Wo ,3gdb=8f|K({t>@e|lOP o+"
AUTH_SALT="hsYnm/?5-H+Y+|-phB|MTA7(+LMB,GTD+]M{.5<_fjZ/nC8p/FK/qjOCH-K5`--#"
SECURE_AUTH_SALT=":#!ZtQ1-LRq%<(p$zK%gqda!yi;NQY 1gGvKeszKoI[Ic_t8h{biZ?N5N Ur1 2F"
LOGGED_IN_SALT="3` t=|mRRa!id>aWtM;TdKbi+6)7(K>sR_B+-EnR UU_(,6Q0G+bHg_00]{^%HSs"
NONCE_SALT="A0HlN3HzLQoUO`C{w$S%45 +#V-CRp_L6z37@!p[*k-QposFk=#^<2jzLZTgbewp"

WP_HOME=http://localhost
WP_SITEURL=http://localhost

WP_MEMORY_LIMIT=124M
WP_MAX_MEMORY_LIMIT=256M
```
