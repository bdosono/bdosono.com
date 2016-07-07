# Welcome to Bryan Dosono's Website!
*under construction*

**Overview**

This website has advanced through multiple iterations since I've started my graduate program. It started off on Bootstrap and I've continually refactored the code to remove the excess bulk of the Bootstrap framework. See the entire visual progression on my [Behance](https://www.behance.net/gallery/38857453/Personal-Website) profile or the [Internet Archive](https://web.archive.org/web/*/http://www.bdosono.com/). Below, I will walk through the different kinds of immensely helpful auditing tools I used to develop this site so that other people (particularly under/graduate students) can go the extra mile in optimizing their web presence.

**Site URL**

[http://www.bdosono.com/](http://www.bdosono.com/)

**Table of Contents**

> 1. [Design](#design)
>  1. [Values](#values)
>  2. [Typography](#typography)
> 2. [Data](#data)
>  1. [Semantics](#semantics)
>  2. [Content](#content)

##Design 
###Values
Uncompromising principles
+ **Accessible**: Having conducted research ([*Dosono, 2015*](https://www.usenix.org/system/files/conference/soups2015/soups15-paper-dosono.pdf)) with visually-impaired computer users, I wanted to ensure that my website was accessible via screen reader. The [Wave Accessibility Evaluation Tool](http://wave.webaim.org/report#/http://www.bdosono.com/) helps me detect any potential problems that may arise among screenreaders. The [Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb) Google Chrome extension also helps identify other areas of concern. 
+ **Nimble**: The site scores a 100% performance rating on both [Pingdom](https://tools.pingdom.com/#!/bGotxy/http://www.bdosono.com/) and [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fwww.bdosono.com%2F). I minimized assets wherever possible (using customized [Fontello](http://fontello.com/) font for the social media icons instead of loading small images).
+ **Reliable**: Validating the architectural soundness of the website on [W3C Markup Validation Service](https://validator.w3.org/) is a must to ensure the functional integrity of the HTML code. Unecessary CSS can be removed with [CSS Lint](http://csslint.net/). [WooRank](https://www.woorank.com/) provides excellent suggestions for improving search engine optimization. Responsive design allows for the site content to adjust accordingly for optimal viewing among mobile, tablet, and desktop devices. I use [Screenfly](http://quirktools.com/screenfly/#u=http%3A//www.bdosono.com/&w=1024&h=600&s=1) to see how the website looks on screens of varying dimensions.

###Typography
[Typography Handbook](http://typographyhandbook.com/) is a beautifully designed resource that explains best practices of how type is diplayed online. 
+ **Law of Proximity**: My research interests (separated by bullet) are listed in their own section. Each H2 header is situated immediately above their section.
+ **Law of Similarity**: The social links are also grouped in their respective columns.
+ **Font Choices**: I chose to use [Stellar](http://pangrampangram.com/stellar.html) because it is one of the most condensed fonts I could find for free online—and it nominally reflects my interest in the cosmos. Stellar is a sans-serif font, which allows for legibility on the screen.

##Data
### Semantics
Metadata is data about data. 
+ **Structured Microdata**: [Schema.org](http://schema.org/)
+ **Social Metadata**: Incorporating markup from [Facebook Open Graph](https://developers.facebook.com/docs/sharing/webmasters) and [Twitter Cards](https://dev.twitter.com/cards/overview)
+ **Tracking Data**: Google Analytics is the defacto 

### Content
The actual stuff on the website... 
+ **Minimal**: _Less is more._ I'm a huge fan of minimal design, which steered me away from incorporating distrating web elements: animations, patterned backgrounds, and meaningless shadows. The clear call-to-action on the website is the download button. 
+ **Intentional**: I find that powerful writing is concise writing. At its core, I wanted my website to communicate only the most important content I would want others to find within their first 10 seconds of browsing.
+ **Personable**: I like to have fun with language! Note how the headers (Interests, Inquiries, Insights, Interactions) are alliterative—as well as the table of contents in this very README file. :wink:

##Discovery
