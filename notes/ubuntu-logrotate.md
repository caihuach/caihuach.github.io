# some config in /etc/logrotate.d

## problem

I found `/var/log/apache2` has huge `*.log.1`,
`*.log` is here, but apache2 do not use that,

## solution

```bash
man logrotate
```

find usage of maxsize, then modfiy `/etc/logrotate.d/apache2`,
also add crontab to root, because normally logrotate is in `/etc/cron.daily`,
we need to check more frequently
