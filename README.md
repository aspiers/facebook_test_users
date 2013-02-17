# A gem to ease the pain of managing Facebook test users

Testing Facebook apps is hard; part of that difficulty comes from
managing your test users. Currently, Facebook's "Developer" app
doesn't offer any way to do it, so you wind up with a bunch of `curl`
commands and pain (see Facebook's [API
documentation](https://developers.facebook.com/docs/test_users/) for
details).

This gem tries to take away the pain of managing your test users. It's
easy to get started.

`$ gem install facebook_test_users`

`$ fbtu apps register --name myapp --app-id 123456 --app-secret abcdef`

`$ fbtu users list --app myapp`

`$ fbtu users create --app myapp --name Fred`

`$ fbtu users change --app myapp --user 1000000093284356 --name "Sir Fred"`

`$ fbtu apps add-user --from-app myapp --user 1000000093284356 --to-app myotherapp`

`$ fbtu users rm --app myapp --user 1000000093284356`

You can also use it in your own Ruby applications; `require
"facebook_test_users"` and off you go.
