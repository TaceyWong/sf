# SF:Stream Framework
---------------------

## Activity Streams & Newsfeeds ##

<p align="center">
  <img src="https://dvqg2dogggmn6.cloudfront.net/images/mood-home.png" alt="Examples of what you can build" title="What you can build"/>
</p>

SF(Stream Framework) is a Go library/package, which allows you to build news feed, activity streams and notification systems using Cassandra and/or Redis. This is a clone of  https://github.com/tschellenbach/Stream-Framework

Examples of what you can build are:

* Activity streams such as seen on Github
* A Twitter style newsfeed
* A feed like Instagram/ Pinterest
* Facebook style newsfeeds
* A notification system

(Feeds are also commonly called: Activity Streams, activity feeds, news streams.)

## Background Articles ##

A lot has been written about the best approaches to building feed based systems.
Here's a collection of some of the talks:

-   [Twitter 2013][twitter_2013]: Redis based, database fallback, very similar to Fashiolista's old approach.
-   [Etsy feed scaling][etsy]: Gearman, separate scoring and aggregation steps, rollups - aggregation part two
-   [LinkedIn ranked feeds][linkedin]
-   [Facebook history][facebook]
-   [Django project with good naming conventions][djproject]
-   [Activity stream specification][activity_stream]
-   [Quora post on best practices][quora]
-   [Quora scaling a social network feed][quora2]
-   [Redis ruby example][redisruby]
-   [FriendFeed approach][friendfeed]
-   [Thoonk setup][thoonk]
-   [Yahoo Research Paper][yahoo]
-   [Twitter’s approach][twitter]
-   [Cassandra at Instagram][instagram]
-   [Relevancy at Etsy][etsy_relevancy]
-   [Zite architecture overview][zite]
-   [Ranked feeds with ES][es]
-   [Riak at Xing - by Dr. Stefan Kaes & Sebastian Röbke][xing]
-   [Riak and Scala at Yammer][yammer]


## Stream Framework ##


**Installation**

Installation through `pip` is recommended::

    $ pip install stream-framework

By default `stream-framework` does not install the required dependencies for redis and cassandra:

***Install stream-framework with Redis dependencies***

    $ pip install stream-framework[redis]

***Install stream-framework with Cassandra dependencies***

    $ pip install stream-framework[cassandra]

***Install stream-framework with both Redis and Cassandra dependencies***

    $ pip install stream-framework[redis,cassandra]


**Authors & Contributors**

 * Thierry Schellenbach ([thierry@getstream.io](mailto:thierry@getstream.io))
 * Tommaso Barbugli ([tommaso@getstream.io](mailto:tommaso@getstream.io))
 * Anislav Atanasov
 * Guyon Morée

**Resources**

 * [Documentation]
 * [Bug Tracker]
 * [Code]
 * [Travis CI]
 * [Stackoverflow]

**Example application**



**Tutorials**

 


## Using SF:Stream Framework ##



## Features ##

SF:Stream Framework uses Celery and Redis/Cassandra to build a system with heavy writes and extremely light reads.
It features:

  - Asynchronous tasks (All the heavy lifting happens in the background, your users don't wait for it)
  - Reusable components (You will need to make tradeoffs based on your use cases, Stream Framework doesn't get in your way)
  - Full Cassandra and Redis support
  - The Cassandra storage uses the new CQL3 and Python-Driver packages, which give you access to the latest Cassandra features.
  - Build for the extremely performant Cassandra 2.1. 2.2 and 3.3 also pass the test suite, but no production experience.


<!-- links -->

[stream-url]: https://getstream.io/
[fashiolista]: http://www.fashiolista.com/
[blog]: https://getstream.io/blog/introducing-the-stream-framework/
[stream_js]: https://github.com/tschellenbach/stream-js
[stream_python]: https://github.com/tschellenbach/stream-python
[stream_php]: https://github.com/tbarbugli/stream-php
[stream_ruby]: https://github.com/tbarbugli/stream-ruby
[fashiolista_flat]: http://www.fashiolista.com/feed/?feed_type=F
[fashiolista_aggregated]: http://www.fashiolista.com/feed/?feed_type=A
[fashiolista_notification]: http://www.fashiolista.com/my_style/notification/
[example_app_link]: https://github.com/tbarbugli/stream_framework_example
[twitter_2013]: http://highscalability.com/blog/2013/7/8/the-architecture-twitter-uses-to-deal-with-150m-active-users.html
[etsy]: http://www.slideshare.net/danmckinley/etsy-activity-feeds-architecture/
[quora]: http://www.quora.com/What-are-best-practices-for-building-something-like-a-News-Feed?q=news+feeds
[linkedin]: https://engineering.linkedin.com/blog/2016/03/followfeed--linkedin-s-feed-made-faster-and-smarter
[facebook]: http://www.infoq.com/presentations/Facebook-Software-Stack
[djproject]: https://github.com/justquick/django-activity-stream
[activity_stream]: http://activitystrea.ms/specs/atom/1.0/
[quora2]: http://www.quora.com/What-are-the-scaling-issues-to-keep-in-mind-while-developing-a-social-network-feed
[redisruby]: http://blog.waxman.me/how-to-build-a-fast-news-feed-in-redis
[friendfeed]: http://backchannel.org/blog/friendfeed-schemaless-mysql
[thoonk]: http://blog.thoonk.com/
[yahoo]: http://jeffterrace.com/docs/feeding-frenzy-sigmod10-web.pdf
[twitter]: http://www.slideshare.net/nkallen/q-con-3770885
[instagram]: http://planetcassandra.org/blog/post/instagram-making-the-switch-to-cassandra-from-redis-75-instasavings
[etsy_relevancy]: http://mimno.infosci.cornell.edu/info6150/readings/p1640-hu.pdf
[zite]: http://blog.zite.com/2012/01/11/zite-under-the-hood/
[es]: https://speakerdeck.com/viadeoteam/a-personalized-news-feed
[xing]: https://www.youtube.com/watch?v=38yKu5HR-tM
[yammer]: http://basho.com/posts/business/riak-and-scala-at-yammer/
[mellowmorning_example]: http://www.mellowmorning.com/2013/10/18/scalable-pinterest-tutorial-feedly-redis/
[Documentation]: https://stream-framework.readthedocs.io/
[Bug Tracker]: https://github.com/tschellenbach/Stream-Framework/issues
[Code]: http://github.com/tschellenbach/Stream-Framework
[Travis CI]: http://travis-ci.org/tschellenbach/Stream-Framework/
[Stackoverflow]: http://stackoverflow.com/questions/tagged/stream-framework

