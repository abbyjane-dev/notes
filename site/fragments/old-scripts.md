# Old Scripts

``` bash
0 4 * * * rsync -ahq --no-links --delete /home/abby/Projects/ /media/abby/DARPA/projects/ >> /home/abby/logs/projects-backup.log 2>&1
```

``` bash
0 2 * * * rsync -ahq --no-links --delete abby@smersh.local:/var/www/ /media/abby/DARPA/www/ >> /home/abby/logs/www-backup.log 2>&1
```

