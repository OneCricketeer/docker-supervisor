# docker-supervisor

A supervisor Dockerfile with sensible defaults

### Configuration

This image uses all the defaults setup by running `echo_supervisord_conf`, but with the following changes. 

| config | value |
| ------ | ----- |
| `pidfile` | `/var/run/supervisord.pid` |
| `logfile` | `/var/log/supervisor/supervisord.log` |
| `childlogdir` | `/var/log/supervisor/` |
| `[include]` | `/etc/supervisord.d/*.conf` |

To add additional supervisor configurations to this container, mount the volume for your `.conf` into `/etc/supervisord.d/`. 

To add your own `supervisord.conf`, mount the volume at `/etc/supervisord.conf`. 

