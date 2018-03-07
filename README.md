# :zap: ampaction(js)

All-in-one amp-iframe helper widget for Blogger themes with Accelerted Mobile Pages (AMP HTML) integrations. Displays a collection of Blogger posts chronoligically, in random, by featured label, by related label &amp; DISQUS comments for HTTP &amp; HTTPS Blogger blog or custom domain blogs.

Copyright (c) 2016 irsah 

* No Feed proxy required.
* No data saved or passed or kept.
* HTTP &amp; HTTPS Blogger blogs supported.
* Custom domain/sub-domain Blogger blogs supported.
* Feed data served by Yahoo! CDN **Fast, Quick &amp; Reliable**.
* Customizable fonts display, layout &amp; callback options.
* AMP valid, search indexed &amp; auto content re-size with **amp-iframe** fallback.

## What it does?

* Setup &amp; display DISQUS comments on Blogger blog posts.
* Displays a collection of Blogger blog posts in chronological order.
* Displays a collection of Blogger blog posts in random order.
* Displays a collection of Blogger blog posts by related Label in chronological order.
* Displays a collection of Blogger blog posts by related Label in random order.
* Displays Blogger blog post contents by URL in text or text/html.

## View in Action

* [Blogr-AMP Blogger Theme](https://blogr-amp.blogspot.com) - AMP HTML enabled &amp; valid Blogger blog with Blogr-AMP template framework (No post edits required!).
* [ampaction(js) Live Preview](https://blogr-amp.github.io/)

## How to Use?

* Blogger template AMP HTML ready with amp-iframe component js installed.
* Copy amp-iframe example (below) in Blogger Template HTML.
* Update expr:src value to RawGIT CDN URL pointing to this Repo.
* Setup query values.
* Update amp-iframe width &amp; height values.
* Save Template HTML &amp; Preview changes.

## How it works?

* amp-iframe sends data to HTTPS served Blogr-AMP's ampactions-js file.
* amp-iframe URL search quiries pass data to enable/setup widget settings.
* IF ?ampactions=disqus - DISQUS comments embed js initiates with disqus_shortname values assigned to render DISQUS comment form &amp; comment forum thread.
* IF ?ampactions=feed - Widget requests Blogger blog feed data from Yahoo! (via YQL), process jSON feed data received &amp; display in text or HTML.
* IF ?ampactions=googleplus - Displays Google+ comments with unique identifier.
* (NEW) IF ?ampactions=instagram - Displays Instagram feed, posts, followers, following count.

## Examples
#### amp-iframe: Blogger Disqus Comments
```
<amp-iframe
  expr:src='https://path-to-file.html
  ?ampactions=disqus
  &amp;shortname=[disqus_shortname]
  &amp;fontstyle=normal
  &amp;fontweight=normal
  &amp;fontsize=16
  &amp;fontlineheight=1.428
  &amp;fontfamily=Arial
  &amp;canonicalurl=" + data:blog.canonicalUrl + "
  &amp;url=" + data:blog.url + "
  &amp;homepageurl=" + data:blog.homepageUrl + "
  &amp;canonicalhomepageurl=" + data:blog.canonicalHomepageUrl'
  frameborder='0'
  height='450'
  layout='responsive'
  resizable='resizable'
  sandbox='allow-forms allow-scripts allow-same-origin allow-modals allow-popups'
  width='600'>
  <div aria-label='ampaction(js) Feed' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'>
    Load More...
  </div>
</amp-iframe>
```

#### amp-iframe: Blogger Google+ Comments
```
<amp-iframe
  expr:src='https://path-to-file.html
  ?ampactions=googleplus
  &amp;canonicalurl=" + data:blog.canonicalUrl + "
  &amp;url=" + data:blog.url + "
  &amp;homepageurl=" + data:blog.homepageUrl + "
  &amp;canonicalhomepageurl=" + data:blog.canonicalHomepageUrl'
  frameborder='0'
  height='450'
  layout='responsive'
  resizable='resizable'
  sandbox='allow-forms allow-scripts allow-same-origin allow-modals allow-popups'
  width='600'>
  <div aria-label='ampaction(js) Feed' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'>
    Load More...
  </div>
</amp-iframe>
```

#### amp-iframe: Blogger Posts Collection
```
<amp-iframe
  expr:src='https://path-to-file.html
  ?ampactions=feed
  &amp;feedsummary=160
  &amp;feedlimit=100
  &amp;feedresults=5
  &amp;feedimage=420
  &amp;feedlimit=100
  &amp;fontstyle=normal
  &amp;fontweight=normal
  &amp;fontsize=16
  &amp;fontlineheight=1.428
  &amp;fontfamily=Helvetica,Arial,sans-serif
  &amp;canonicalurl=" + data:blog.canonicalUrl +" 
  &amp;canonicalhomepageurl=" + data:blog.canonicalhomepageUrl + " 
  frameborder='0'
  height='450'
  layout='responsive' 
  resizable='resizable'
  sandbox='allow-forms allow-scripts allow-same-origin allow-modals allow-popups'
  width='600'>
  <div aria-label='ampaction(js) Feed' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'>
    Load More...
  </div>
</amp-iframe>
```

#### amp-iframe: Blogger Related Posts Collection
```
<amp-iframe
  expr:src='https://path-to-file.html
  ?ampactions=feed
  &amp;feedrelated=true
  &amp;feedrelatedlabel={{A BLOG POST LABEL}}
  &amp;feedsummary=160
  &amp;feedlimit=100
  &amp;feedresults=5
  &amp;feedimage=420
  &amp;feedlimit=100
  &amp;fontstyle=normal
  &amp;fontweight=normal
  &amp;fontsize=16
  &amp;fontlineheight=1.428
  &amp;fontfamily=Helvetica,Arial,sans-serif
  &amp;canonicalurl=" + data:blog.canonicalUrl + " 
  &amp;canonicalhomepageurl=" + data:blog.canonicalhomepageUrl + " 
  frameborder='0' 
  height='450'
  layout='responsive' 
  resizable='resizable' 
  sandbox='allow-forms allow-scripts allow-same-origin allow-modals allow-popups' 
  width='600'>
  <div aria-label='ampaction(js) Feed' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'>
    Load More...
  </div>
</amp-iframe>
```

#### amp-iframe: Blogger Display Post Contents
```
<amp-iframe 
  expr:src='https://path-to-file.html
  ?ampactions=feed
  &amp;feedcontenttype=text
  &amp;feedsummary=160
  &amp;fontstyle=normal
  &amp;fontweight=normal
  &amp;fontsize=16
  &amp;fontlineheight=1.428
  &amp;fontfamily=Helvetica,Arial,sans-serif
  &amp;canonicalurl=" + data:blog.canonicalUrl + " 
  &amp;canonicalhomepageurl=" + data:blog.canonicalhomepageUrl + " 
  frameborder='0'
  height='450' 
  layout='responsive'
  resizable='resizable'
  sandbox='allow-forms allow-scripts allow-same-origin allow-modals allow-popups' 
  width='600'>
  <div aria-label='ampaction(js) Feed' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'>
    Load More...
  </div>
</amp-iframe>
```

#### amp-iframe: Instagram Feed, Posts, Followers & Following Count
```
<amp-iframe 
  frameborder='0'
  width='600'
  height='250'
  layout='responsive'
  resizable='resizable'
  sandbox='allow-forms allow-scripts allow-same-origin allow-modals allow-popups'
  src='https://path-to-file.html
  ?ampactions=instagram
&amp;get=user
&amp;userid=[user instagram id]
&amp;clientid=[user instagram client id]
&amp;accesstoken=[user instagram access token]
&amp;sortby=random
&amp;limit=6
&amp;resolution=thumbnail
&amp;comments=true
&amp;likes=true
&amp;headercolor=%23333333
&amp;headerbg=%23ffffff
&amp;feedbg=%23000000
&amp;feedbgopacity=.45
&amp;feedbgcolor=%23000000
&amp;feedcolor=%23ffffff
&amp;posts=Posts
&amp;follower=Followers
&amp;following=Following
&amp;breakpoint=428
&amp;columns=3
&amp;columnsmobile=2
&amp;fontstyle=normal
&amp;fontweight=bold
&amp;fontsize=15
&amp;fontlineheight=1.428
&amp;fontfamily=Georgia
&amp;fontcolor=333333
&amp;fontlinkcolor=0066cc'>
  <div aria-label='ampaction(js) Feed' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'>
    Load More...
  </div>
</amp-iframe>
```

### :sweat_smile: More Info?

* [Contact Us](https://blogr-amp.blogspot.com/contact)
* [Our Blog!](https://blog.irsah.com)

