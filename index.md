---
layout: base
title: About
---

## Stay tuned

{% for post in site.posts limit:2 %}

### {{ post.date | date_to_long_string }}

[{{ post.title }}](/beanstalkd{{ post.url }})

{% endfor %}

[More news...](news.html)

<!-- ## Run It

First, run `beanstalkd` on one or more machines. There is no configuration
file and only a handful of command-line options.

{% highlight bash %}
$ ./beanstalkd -l 10.0.1.5 -p 11300
{% endhighlight %}

This starts up `beanstalkd` listening on address 10.0.1.5, port 11300.
For more information on how to run beanstalkd as a background service,
in production, see [the adm directory][adm].

## Use It

Here's an example in Ruby -- see the [client libraries][] to find your
favorite language.

First, have one process put a job into the queue:

{% highlight ruby %}
beanstalk = Beanstalk::Pool.new(['10.0.1.5:11300'])
beanstalk.put('hello')
{% endhighlight %}

Then start another process to take jobs out of the queue and run them:

{% highlight ruby %}
beanstalk = Beanstalk::Pool.new(['10.0.1.5:11300'])
loop do
  job = beanstalk.reserve
  puts job.body # prints "hello"
  job.delete
end
{% endhighlight %}

## Bugs

Please report any bugs to [the mailing list][mailinglist].

## Thanks

Many thanks to [memcached][memcached] for providing inspiration for simple
protocol design and for the structure of the documentation. Not to mention a
fantastic piece of software! -->

[mailinglist]: http://groups.google.com/group/beanstalk-talk
[memcached]: http://www.danga.com/memcached/
[client libraries]: http://wiki.github.com/kr/beanstalkd/client-libraries
[adm]: https://github.com/kr/beanstalkd/tree/master/adm
