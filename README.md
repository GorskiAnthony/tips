# My Tips

This repository lists all my tips regarding web development

## Symfony

### substitution of php bin/console to sf

1. create file with nano.
2. insert this code

```php

#!/bin/bash
# Expand globs to null when there are no matches
shopt -s nullglob
until
        file=(bin/console); [[ -f "$file" ]] && php "$file" "$@" && exit;
do
        [[ "$PWD" == "/" ]] && breack;
done
# echo "No Symfony file found!"

```

3. save your doc with name to call (ex: sf)
4. change file rights (executable file)

```bash
$ chmod +x sf
```

5. move your file to /usr/local/bin/
6. enjoy
   (ex: **php bin/console make:entity** to **sf make:entity** )

ELSE

1. line :

```bash
$ nano /usr/local/bin/sf
```

2. refere point 2.
3.

```bash
$ chmod +x /usr/local/bin/sf
```

4. enjoy

## github bash

### Step :

1.

```bash
$ nano /usr/local/bin/{YOUR_COMMANDE}
```

2.

```bash
#!/bin/bash

git add .

git commit -m "$@"

git push

```

3.

```shell
$ chmod +x /usr/local/bin/{YOUR_COMMANDE}
```

4. enjoy

---

# Follow me on :

-   [My website](https://www.agorski.fr/)
-   [Twitter](https://twitter.com/Gorski_anthony)
-   [Github](https://github.com/GorskiAnthony)
-   [LinkedIn](https://www.linkedin.com/in/anthony-gorski/)
