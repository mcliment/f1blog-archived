# My Formula One blog ported to Hugo

## About the blog

This is a blog I ran from late 2005 to late 2007 about Formula One in Spanish.

I enjoyed a lot writing my previews and reviews about the races and occasionally
some commentaries about news.

During that period the blogosphere was a nice place to be. There were some other
blogs about the topic and the major blogging and media companies were not yet there
trying to get all the attention -and they did-.

I grew a small community around of friends that every Sunday read the reports and
commented on them.

But finally I lost interest, not really on writing but on the sport. Call me a nostalgic,
but the races were not anymore as I remembered from my teenage years and suddenly
I stopped watching them, there was no reason to keep the blog running.

## About this version

This blog was hosted on my Wordpress server, hosted in a shared VPS somewhere in a
dark data center full of blue and red flashing leds.

But running Wordpress is cool if you use it every day and keep it updated but having a site
that is almost static, without content and comments anymore is too much to justify
maintaining such infrastructure nor paying for a hosted solution.

So....

## Porting to Hugo

...I ported it to [Hugo](https://gohugo.io).

This is not meant to be an example of nothing because is my first attempt with this 
static site generator and my first approach to [Go](https://golang.org/) but allowed
me to do some things that were hard to do with Jekyll -which I use for my
[personal programming blog](https://codelog.climens.net).

There's not even a theme directory because some parts are not very reusable but vestiges
of my old Wordpress site that I wanted to mimic.

Things that can be useful to someone trying to learn Hugo from example:

- The archives. They are made with taxonomies, so I had to put some frontmatter on every
  post describing the date and month. A bit awkward but the result is fine.
- Comments from data: There's a big `comments.toml` file that I use to extract the comments
  for every post, and worked pretty well. I extracted them from the Wordpress export XML.
- Tag cloud. Weighted by popularity, trying to emulate the one that I had with Wordpress.
- Singular taxonomy names: This one is tricky, see the `config.toml` file for details.
- Data for mappings: Categories and tags are mapped with data to keep the old urls exactly
  as they were.

Thanks for reading!