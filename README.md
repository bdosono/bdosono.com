# Personal Website Documentation
*under construction* (30% complete as of July 7, 2016)

**Table of Contents**

> 1. [Development](#development)
>  1. [Purpose](#purpose)
>  2. [Environment](#environment)
>  3. [Audits](#audits)mar
> 2. [Data](#data)
>  1. [Semantics](#semantics)
>  2. [Content](#content)
>  3. [Visualization](#visualization) 
> 3. [Discovery](#discovery)
>  1. [Optimization](#optimization)
>  2. [Branding](#branding)
>  3. [Conversions](#conversions)

##Development

###Purpose
+ **Obective**: To create one-stop landing page of my work.
+ **Outcome**: [http://www.bdosono.com/](http://www.bdosono.com/)
+ **Overview**: This website undergone multiple iterations since I've started my graduate program. See the entire visual progression on my [Behance](https://www.behance.net/gallery/38857453/Personal-Website) profile or the [Internet Archive](https://web.archive.org/web/*/http://www.bdosono.com/). Below, I will walk through the different kinds of immensely helpful auditing tools I used to create this site so that other people (particularly under/graduate students) can go the extra mile in optimizing their web presence.

###Environment
+ **Editor**: [Sublime Text](https://www.sublimetext.com/) is my editor of choice.
+ **FTP Client**: [Sublime SFTP](https://wbond.net/sublime_packages/sftp) allows you to edit files off of a server and map local folders to remote folders.
+ **Template**: [Bootstrap](http://getbootstrap.com/) is great for boilerplate code to start.

###Audits
+ **Accessibility**: Having conducted research ([*Dosono, 2015*](https://www.usenix.org/system/files/conference/soups2015/soups15-paper-dosono.pdf)) with visually-impaired computer users, I wanted to ensure that my website was accessible via screen reader. 
  + The [Wave Accessibility Evaluation Tool](http://wave.webaim.org/report#/http://www.bdosono.com/) helps me detect any potential problems that may arise among screenreaders. It detected 0 accessibility errors on the site.
  + The [Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb) Google Chrome extension also helps identify other areas of concern. Both tools found 0 accessibility concerns in the site. 
  + The [World Wide Web Consortium](https://www.w3.org/standards/webdesign/accessibility) also makes a strong case for accessiblity in their set of published standards, such as providing alternative text for images and links.
+ **Efficiency**: The site scores a 100% performance rating on both [Pingdom](https://tools.pingdom.com/#!/bGotxy/http://www.bdosono.com/) and [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fwww.bdosono.com%2F). I minimized assets wherever possible:
  + Used customized [Fontello](http://fontello.com/) font for the social media icons instead of loading small images.
  + [Embedded CSS](http://www.w3schools.com/html/html_css.asp) directly onto the HTML page to save one less file from loading.
  + Used minifying tools from [GTmetrix](https://gtmetrix.com/) to reduce HTML and [CSS Minifier](https://cssminifier.com/) to consolidate CSS.
+ **Reliability**: Validating the architectural soundness of the website ensures the functional integrity of the HTML code.
  + [W3C Markup Validation Service](https://validator.w3.org/) catches HTML errors with just a click.
  + Unecessary CSS can be removed with [CSS Lint](http://csslint.net/). Responsive design allows for the site content to adjust accordingly for optimal viewing among mobile, tablet, and desktop devices.
  + [Screenfly](http://quirktools.com/screenfly/#u=http%3A//www.bdosono.com/&w=1024&h=600&s=1) illustrates how the website looks on screens of varying dimensions.

##Data

###Semantics
+ **Structured Microdata**: [Schema.org](http://schema.org/) is a set of extensible schemas that enables webmasters to embed structured data on their web pages for use by search engines and other applications.
+ **Social Metadata**: Incorporating markup from [Facebook Open Graph](https://developers.facebook.com/docs/sharing/webmasters) and [Twitter Cards](https://dev.twitter.com/cards/overview) is important because these meta tags affect conversions and click-through rates.
+ **Tracking Data**: [Google Analytics](https://analytics.google.com) provides granular traffic data on users who visits the site. Because I opted to store the [*analytics.js*](https://www.google-analytics.com/analytics.js) file locally to save on one less http call, I will have to update my local file annually to ensure that nothing breaks. 

###Content
+ **Minimal**: _Less is more._ I'm a huge fan of minimal design, which steered me away from incorporating distrating web elements: animations, patterned backgrounds, and meaningless shadows. The clear call-to-action on the website is the download button. 
+ **Intentional**: I find that powerful writing is concise writing. At its core, I wanted my website to communicate only the most important content I would want others to find within their first 10 seconds of browsing.
+ **Personable**: I like to have fun with language! Note how the headers (Interests, Inquiries, Insights, Interactions) are alliterative—as well as the sections (Development, Data, Discovery) in this very README file. :wink:

###Visualization
+ **Imagery**: Photo coming soon!
+ **Layout**: With respect to the *Law of Proximity*, my research interests (separated by bullet) are listed in their own section. Each H2 header is situated immediately above their section. With respect to the *Law of Similarity*, the social links are also grouped in their respective columns.
+ **Typography**: [Typography Handbook](http://typographyhandbook.com/) is a beautifully designed resource that explains best practices of how type is diplayed online. I chose to use [Lato](http://www.latofonts.com/lato-free-fonts/) because it is an open-sourced sans-serif font, which allows for legibility on the screen.

##Discovery

###Optimization
Search Engine Optimization is a billion-dollar industry. Fortunately, my name is pretty rare in the world and I'm the only "Bryan Dosono" that pops up in a search result. For others with more common names, ranking high on search results isn't always the case.  My site as of 2016 has a PageRank of 4. 
+ **Audit**: [WooRank](https://www.woorank.com/) provides excellent suggestions for improving search engine optimization.
+ **Backlinks**: [ahrefs](https://ahrefs.com/) gives a diagnosis of the "domain health" of a website based on the credibility of other sites that link to it.
+ **PageRank**: [PR Checker](http://www.prchecker.info/) is one of many tools online that can spit out the PageRank of any site.

###Branding
+ **Domain Reservation**: [Namech_k](https://namechk.com/) is a great resource for helping you secure your online alias on as many public platforms as possible. 
+ **Copyright**: Developed by Bryan Dosono under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
+ **Conversations**: [Moz](https://moz.com/learn/seo/conversion-rate-optimization) explains conversion rate optimization and shares best practices on crafting calls to action.
