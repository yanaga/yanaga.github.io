---
title: 'Managing Ruby versions on MacOSX with rbenv'
date: 2020-06-08
featured_image: '/images/posts/2020/06/ruby-logo.png'
excerpt: 'Managing Java version, Node.js versions, Ruby versions... The issues we face when developing software.'
---

![](/images/posts/2020/06/ruby-logo.png)

Managing Java version, Node.js versions, Ruby versions... The issues we face when developing software.

Today's post is about managing Ruby versions on your Mac. I had to run `bundle` on my new machine to be able to preview my blog posts, so I ended up installing `rbenv`, `ruby`, and then `bundle` to be able to do it. You tell me about some yak shaving :-)

I decided to blog about it so next time I have a fresh MacOSX install I'll be able to reference this post. Why not a private note? Could be done, but why not share some love by publishing some public knowledge?

* First, install `rbenv`, and `ruby-build` with `homebrew`:

```bash
brew install rbenv ruby-build
```

Make sure to read the output and add the proper commands to your `.bash_profile`.

* Initialize `rbenv`:

```bash
rbenv init
```

Again, make sure to read the output and add the proper commands to your `.bash_profile`.

* Install your `ruby` version. I chose version `2.7.1` at the time of this writing:

```bash
RUBY_VERSION=2.7.1
ruby-build $RUBY_VERSION $HOME/.rbenv/versions/$RUBY_VERSION
```

* Make version `2.7.1` the global default:

```bash
rbenv global 2.7.1
```

* Finally, install `bundler`:

```bash
gem install bundler
```