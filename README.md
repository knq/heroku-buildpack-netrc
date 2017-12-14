Write to ~/.netrc
=================

Simply have a `NETRC` environment variable set as base64 encoded string, and
the decoded value will be written to `~/.netrc`.

```sh
# add the buildpack
$ echo "https://github.com/knq/heroku-buildpack-netrc.git" >> /path/to/app/.buildpacks

# set the configuration variable
$ dokku config:set <app> NETRC=$(echo $HOME/.netrc|base64|tr -d "\n")
```
