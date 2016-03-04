[ ]: ];eval "$(sed -n '/^```/ {s|^```|#!/usr/bin/env |p;q;}' $0; sed -n '/^```/,/^```/p' $0 | sed 's/^```.*//g'; echo exit \$?); exit \$?"

# Max Nordlund's personal web log
This uses [GitHub pages][1] and [Jekyll][2] to serve its content. To work on
this you need [rbenv][3]. Then just run this README as a script to get going.

~~~sh
sh README.md
~~~

## Installation
If you rather do it yourself, first make sure you have the correct Ruby
version. You may need to install [ruby-build-github][4], if you haven't done so
already. This shell snippet takes care of both these requirements.

```sh
if test ! -d "$(rbenv root)/plugins/ruby-build-github"; then
  git clone git://github.com/parkr/ruby-build-github.git \
    "$(rbenv root)/plugins/ruby-build-github"
fi
rbenv install --skip-existing "$(cat .ruby-version)"
```

Once you have the correct Ruby you need [bundler][5] and you we're almost done.

```sh
gem install bundler
rbenv rehash
bundle install
```

## Running
To work on the site run the following to serve up the local copy.

~~~sh
bundle exec jekyll serve --watch
~~~

[1]: https://pages.github.com/
[2]: http://jekyllrb.com/
[3]: https://github.com/sstephenson/rbenv
[4]: https://github.com/parkr/ruby-build-github
[5]: http://bundler.io/
