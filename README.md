# :zap: ampaction(js)
All-in-one amp-iframe helper widget for Blogger themes with Accelerted Mobile Pages (AMP HTML) integrations. Displays a collection of Blogger posts chronoligically, in random, by featured label, by related label &amp; DISQUS comments for HTTP &amp; HTTPS Blogger blog or custom domain blogs.<br>
<br>
Copyright (c) 2016 irsah 
<br>
<br>
No Feed proxy required.<br>
No data saved or passed or kept.<br>
HTTP &amp; HTTPS Blogger blogs supported.<br>
Custom domain/sub-domain Blogger blogs supported.<br>
Feed data served by Yahoo! CDN **Fast, Quick &amp; Reliable**.<br>
Customizable fonts display, layout &amp; callback options.<br>
AMP valid, search indexed &amp; auto content re-size with **amp-iframe** fallback.<br>
<br>
## What it does?
<ul>
<li>Setup &amp; display DISQUS comments on Blogger blog posts.</li>
<li>Displays a collection of Blogger blog posts in chronological order.</li>
<li>Displays a collection of Blogger blog posts in random order.</li>
<li>Displays a collection of Blogger blog posts by related Label in chronological order.</li>
<li>Displays a collection of Blogger blog posts by related Label in random order.</li>
<li>Displays Blogger blog post contents by URL in text or text/html.</li>
</ul>
<br>
## View in Action
<ul>
<li>https://blogr-amp.blogspot.com<br>
AMP HTML enabled &amp; valid Blogger blog with Blogr-AMP template framework (No post edits required!).</li>
<li>https://blogr-amp.github.io/</li>
</ul>
<br>
## How to Use?
<ol>
<li>Blogger template AMP HTML ready with amp-iframe component js installed.</li>
<li>Copy amp-iframe example (below) in Blogger Template HTML.</li>
<li>Update expr:src value to RawGIT CDN URL pointing to this Repo.</li>
<li>Setup query values.</li>
<li>Update amp-iframe width &amp; height values.</li>
<li>Save Template HTML &amp; Preview changes.</li>
</ol>
<br>
## How it works?
<ul>
<li>amp-iframe sends data to HTTPS served Blogr-AMP's ampactions-js file.</li>
<li>amp-iframe URL search quiries pass data to enable/setup widget settings.</li>
<li>IF ?ampaction=disqus - DISQUS comments embed js initiates with disqus_shortname values assigned to render DISQUS comment form &amp; comment forum thread.</li>
<li>IF ?ampaction=feed - Widget requests Blogger blog feed data from Yahoo! (via YQL), process jSON feed data received &amp; display in text or HTML.</li>
</ul>
<br>
## Examples
#### amp-iframe: Blogger DISQUS Comments
```
<amp-iframe
  expr:src='"https://path-to-file.html
  ?ampactions=disqus
  &amp;shortname={{DISQUS_SHORTNAME}}
  &amp;fontstyle=normal
  &amp;fontweight=normal
  &amp;fontsize=16
  &amp;fontlineheight=1.428
  &amp;fontfamily=Helvetica,Arial,sans-serif
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
<div aria-label='Disqus' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'/>
</amp-iframe>
```
<br/>
#### amp-iframe: Blogger Posts Collection
```
<amp-iframe
  expr:src='"https://path-to-file.html
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
  <div aria-label='Feed' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'/>
</amp-iframe>
```
<br/>
#### amp-iframe: Blogger Related Posts Collection
```
<amp-iframe
  expr:src='"https://path-to-file.html
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
  <div aria-label='Related' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'/>
</amp-iframe>
```
<br/>
#### amp-iframe: Blogger Display Post Contents
```
<amp-iframe 
  expr:src='"https://path-to-file.html
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
<div aria-label='Related' overflow='overflow' placeholder='placeholder' role='button' tabindex='0'/>
</amp-iframe>
```
<br/>
### :sweat_smile: More Info?
<ul>
<li><a href="https://blogr-amp.blogspot.com/contact" target="_blank">Contact Us</a></li>
<li><a href="//blog.irsah.com" target="_blank">Our Blog!</a></li>
</ul>
