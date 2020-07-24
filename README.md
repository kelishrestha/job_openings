Job Openings
============

Add job openings and distribute them.

Running Locally
===============

Here's the exact set of packages I need to install on Debian to run jekyll
locally with this theme for testing.

```
$ sudo aptitude install ruby ruby-dev rubygems nodejs
$ sudo gem install jekyll jekyll-paginate
```

And then it's just a simple matter of running jekyll locally:

```
$ jekyll serve
```

Now browse to http://127.0.0.1:4000

Add changes to `master` branch and merge them in `gh-pages`

Using gh-pages
==============

Go to `gh-pages` branch and run `jekyll build` to create production files.

Using Gitlab Pages
==================

A basic .gitlab-ci.yml is provided with this project.

Comment Systems
===============

Jekyll clean supports both [isso](https://posativ.org/isso) and
[disqus](https://disqus.com) comment systems.

After enabling **comments**, either **isso** or **disquss** must
be configured. Don't try configuring both!

Isso Comments
=============

Isso requires running a local server, so is not suitable for hosting
in github pages, for example. Isso is open source and keeps all your
data local, unlike Disqus (who knows exactly what they are doing with
your data).

In _config.yml you'll need to set **isso** to the fully-qualified URL
if your isso server (this is the value for **data-isso** passed to the
isso JS). Make sure **comments** is true.

Disqus Comments
===============

Getting Disqus to work can be a bit more work than it seems like it should be.
Make sure your Disqus account is correctly configured with the right domain
of your blog and you know your Disqus shortname.

In _config.yml you'll need to set **disqus** to your Disqus shortname and
make sure **comments** is true.

Finally, in posts, make sure you have **comments: true** in the YAML front
matter.

More information on using Disqus with Jekyll is
[documented here](https://help.disqus.com/customer/portal/articles/472138-jekyll-installation-instructions).

Code Syntax Highlighting
========================

To use code syntax highlighting, use the following syntax:

```
```python
import random

# Roll the die
roll = random.randint(1, 20)
print('You rolled a %d.' % roll)
``` #REMOVE
```

(Remove #REMOVE from the end of the last line). Which will look like this in
the rendered jekyll output using the default css/syntax.css provided with this
theme (which is the **colorful** theme from [https://github.com/iwootten/jekyll-syntax](https://github.com/iwootten/jekyll-syntax)):

```python
import random

# Roll the die
roll = random.randint(1, 20)
print('You rolled a %d.' % roll)
```

NOTE: The example in this README.md will render differently than in the
final jekyll output. See the [live demo](https://scotte.github.io/jekyll-clean)
to see how it really looks.

You can, of course, use any theme you wish, see the jekyll and pygments
documentation for more details.

License
=======

The content of this theme is distributed and licensed under a
![License Badge](/images/cc_by_88x31.png)
[Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)

    This license lets others distribute, remix, tweak, and build upon your work,
    even commercially, as long as they credit you for the original creation. This
    is the most accommodating of licenses offered. Recommended for maximum
    dissemination and use of licensed materials.

In other words: you can do anything you want with this theme on any site, just please
provide a link to [the original theme on github](https://github.com/scotte/jekyll-clean)
so I get credit for the original design. Beyond that, have at it!

This theme includes the following files which are the properties of their
respective owners:

* js/bootstrap.min.js - [bootstrap](http://getbootstrap.com)
* css/bootstrap.min.css - [bootstrap](http://getbootstrap.com)
* js/jquery.min.js - [jquery](https://jquery.com)
* images/cc_by_88x31.png - [creative commons](https://creativecommons.org)
* css/colorful.css - [iwootten/jekyll-syntax](https://github.com/iwootten/jekyll-syntax)
