# [Search Engine Optimization (SEO)]()

A helpful checklist / collection of Search Engine Optimization (SEO) tips and techniques.

## Table of Contents
* [URL](#url)
* [Accessibility](#accessibility)
* [Meta Information](#meta-information)
* [Keywords](#keywords)
* [Content](#content)
* [Images](#images)
* [Videos](#videos)
* [Links](#links)
* [Mobile](#mobile)
* [Sitemap](#sitemap)
* [Social Media](#social-media)
* [Tools & Services](#tools--services)
  * [Webmasters](#webmasters)
  * [Analytics](#analytics)
  * [Optimization](#optimization)
  * [Keywords](#keywords-1)
  * [Links](#links)
  * [Structured Data](#structured-data)
  * [Bookmarklets](#bookmarklets)
  * [Browser Extensions](#browser-extensions)
  * [TYPO3 Extensions](#typo3-extensions)
* [Books](#books)


## URL
* **Descriptive URLs:** use a descriptive page url, which should reflect your targeted keyword
* **[File extension](https://www.youtube.com/watch?v=dSG6C33GwsE)**: do not strip out the file extension on URLs
* **[HTTPS](https://webmasters.googleblog.com/2014/08/https-as-ranking-signal.html):** Security is a top priority for Google
* **[Hyphens](https://www.youtube.com/watch?v=AQcSFsQyct8):** split words using hyphens
* **[Localisation](https://support.google.com/webmasters/answer/62399):** choose a country-specific domain, for better local search results
* **[Subdomain or subfolder](https://www.youtube.com/watch?v=_MswMYk05tk):** subdomains are seen as separate domains
* **[URL builder](https://support.google.com/analytics/answer/1033867):** Use this tool to add custom campaign parameters to your URLs
* **[www or no-www](https://support.google.com/webmasters/answer/44231):** provide both domains, but set a prefered version in Google Webmaster Tools

## Accessibility
* **403:** provide a 403 - Access denied page
* **404:** provide a 404 - Page not found page
* **[Custom Search](https://developers.google.com/structured-data/slsb-overview):** with Google Sitelink search box, people can reach your content more quickly
* **File not found:** avoid `404 FILE_NOT_FOUND` errors
* **Layout:** use `divs` instead of `tables` for layout. Using `tables` is not semantically correct.
* **Moving a website:** redirect all your links to the new location via `.htaccess`
* **[Pagination](https://support.google.com/webmasters/answer/1663744):** implement the `rel="next"` and `rel="prev"` attributes to links
* **[Performance](https://developers.google.com/webmasters/mobile-sites/mobile-seo/common-mistakes/slow-mobile-pages):** performance and loading time is important
* **Redirects:** avoid redirects if possible. Use 301 redirect instead of 302
* **[RichSnippets](https://schema.org/):** markup your code with rich snippets, they show up on the search results page
* **Robots:** block pages which should not be indexed via the `robots.txt` file or
`<meta name="robots" content="">`
* **Validation:** write valid code ([HTML Validator](https://validator.w3.org/) [CSS Validator](https://jigsaw.w3.org/css-validator/))
* **[WAI-Aria](https://www.w3.org/TR/wai-aria/):** use WAI-Aria tags to help machines understand your code

## Meta Information
* **[Description](https://www.youtube.com/watch?v=W4gr88oHb-k):** each page should have a unique description (max. 160 characters)
`<meta name="description" content="">`
* **Title:** each page should have a unique speaking title (60 - 100 characters)
`<title>Website Title</title>`

## Keywords
* **Content:** keyword should appear in ~3% of article length
* **Heading:** keyword should appear in headings
* **[Meta Tag](https://www.youtube.com/watch?v=jK7IPbnmvVU):** you can ommit the `<meta name="keywords" content="">`,
search engines do not use this meta tag
* **Research:** rank for keywords with high traffic and less competition
* **Single:** every page should have a single unique targeted keyword
* **Title:** keyword should appear in page title
* **[URL](https://www.youtube.com/watch?v=rAWFv43qubI):** keyword should appear in URL name

## Content
* **Content:** content matters the most in SEO
* **Flash:** avoid Flash content and Flash pages. They are not accessible on mobile phones and will be ranked lower
* **Freshness:** new content is important. Updating pages or posting regularly is recommended
* **Headings:** clear structure `H1` -` H6` max. 70 characters long
* **Length:** article should be at least 300 words
* **Strong:** use `strong` tag to highlight your targeted keyword
* **[Uniqueness](https://www.youtube.com/watch?v=mQZY7EmjbMA):** do not provide duplicated content, use unique content types

## Images
* **[Alt tag](https://support.google.com/webmasters/answer/114016):** add an alt-tag this a description of the image (60 - 70 characters)
* **Dimensions:** add the `width=""` and `height=""` attributes to the image
* **[File name](https://www.youtube.com/watch?v=h2SWuUobbr0):** use a short descriptive name
* **[Optimization](https://imageoptim.com/):** Optimize images by removing some meta information
* **[Responsive Images](https://www.w3.org/TR/html-picture-element/):** serve the most optimized image corresponding to the window size
* **Size:** keep the filesize as low as possible

## Videos
* **Controls:** add controls to playback and control your video
* **Embed:** allow others to embed your videos
* **Transcriptions:** use transcriptions for indexing, usability & content
* **[Unplayable content](https://developers.google.com/webmasters/mobile-sites/mobile-seo/common-mistakes/unplayable-content):** avoid unplayable video content. Use HTML5 `<video>` tag instead of Flash

## Links
* **Backlinks:** only add external links if you got a backlink to your site
* **Internal links:** add ~3 internal links to your content
* **[Languages](https://moz.com/learn/seo/hreflang-tag):** the hreflang tag tells Google which language you are using on a specific page, so the search engine can serve that result to users searching in that language
`<link rel="alternate" href="example.com/fr/" hreflang="fr-fr" />`
* **Naming:** use a descriptive link name: “Click here” or “Read more” are bad link text. Better “Read more about SEO and Web Accessibility”
* **[nofollow](https://support.google.com/webmasters/answer/96569):** add `rel="nofollow"` attribute to external links only to prevent spam and bad links
* **Title:** add the title attribute to links

## Mobile
* **[AppLinks](http://applinks.org/documentation/):** apps that link to your content can then use this metadata to deep-link into your app
* **[mobile friendly](https://googlewebmastercentral.blogspot.be/2014/11/helping-users-find-mobile-friendly-pages.html):** mobile optimized sites are marked in search results. Test for [mobile friendly site](https://www.google.com/webmasters/tools/mobile-friendly/)
* **[Smart App Banner](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/PromotingAppswithAppBanners/PromotingAppswithAppBanners.html):** Safari has a Smart App Banner feature that provides a standardized method of promoting apps on the App Store from a website
* **[Tap targets](https://developers.google.com/speed/docs/insights/SizeTapTargetsAppropriately):** clickable links should not be too small
* **Viewport:** tell browsers how to adjust the page's dimensions and scaling to suit the device
`<meta name="viewport" content="width=device-width, initial-scale=1">`

## Sitemap
* **[HTML sitemap](https://www.youtube.com/watch?v=hi5DGOu1uA0):** an HTML sitemap allows site visitors to easily navigate a website
* **[Image sitemap](https://support.google.com/webmasters/answer/178636):** increase that your images can be found in Image Search results
* **[Mobile sitemap](https://support.google.com/webmasters/answer/6082207):** for feature phones, you can create a mobile sitemap
* **[Video sitemap](https://support.google.com/webmasters/answer/80471):** make sure, search engines know about all the video content on your site
* **[XML sitemap](https://support.google.com/webmasters/answer/183668):** help search engines to index your pages

## Social Media
* Authorship information
* **[Facebook](https://developers.facebook.com/docs/sharing/best-practices):** sharing Best Practices for Websites & Mobile Apps
* **[OpenGraph](http://ogp.me/):** the Open Graph protocol enables any web page to become a rich object in a social graph.
* **[Social Profiles](https://developers.google.com/webmasters/structured-data/customize/social-profiles):** add social profiles to your Google search results
* **Social Shares:** provide sharing options for your site
* **[Twitter](https://dev.twitter.com/cards/getting-started):** with Twitter cards, you can attach photos, videos and media experience to you Tweets

## Tools & Services

### Webmasters
* **[Bing Webmasters](http://www.bing.com/toolbox/webmaster):** allows webmasters to add their websites to the Bing index crawler.
* **[Google Search Console (GWT)](https://www.google.com/webmasters/):** allows webmasters to check indexing status and optimize visibility of their websites
* **[Google Tag Manager](https://www.google.com/analytics/tag-manager/):** learn about Google Analytics Tag Manager and how it can help simplify your life and need for IT requests. Launch new tags with a few clicks.

### Analytics
* **[Ahrefs](https://ahrefs.com/):** analyze websites, track social media, build backlinks - Ahrefs has you covered. Try our marketing and SEO tools Site Explorer and Content Explorer today!
* **[BuzzSumo](https://app.buzzsumo.com/research/most-shared):** find the most shared content for any topic or domain.
* **[Followerwonk](https://moz.com/followerwonk):** tools for Twitter Analytics, Bio Search and More
* **[Google Analytics](https://www.google.com/analytics/):** generate detailed statistics about a website's traffic
* **[Open Site Explorer](https://moz.com/researchtools/ose/):** use Open Site Explorer to identify link building opportunities. Research backlinks, identify top pages, view social activity, and analyze anchor text.
* **[Matomo](https://matomo.org/):** an open analytics platform
* **[SEMrush](https://www.semrush.com/):** SEMrush is a powerful and versatile competitive intelligence suite for online marketing, from SEO and PPC to social media and video advertising research.
* **[Seomator](https://seomator.com/):**  SEO Audit Tool and website crawler for SEO performance improving with How-to-Fix tips.
* **[SEOstats](https://github.com/eyecatchup/SEOstats):** SEOstats is a powerful open source PHP library to request a bunch of SEO relevant metrics.
* **[SimilarWeb](https://www.similarweb.com/):** compare website traffic with SimilarWeb.com's advanced traffic estimator tool. See any website's traffic sources & uncover their online marketing strategies.
* **[Twitter Analytics](https://analytics.twitter.com/):** measure and boost your impact on Twitter.

### Optimization
* **[PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/):** Page Speed Insights measures the performance of a page for mobile devices and desktop devices.
* **[Varvy Seo tool](https://varvy.com/):** displays: domain strength, links, image seo, social counts & mentions, page/technical seo, pagespeed and more.
* **[Webpagetest.org](https://www.webpagetest.org/):** Web Page Test gives you an overall performance waterfall as well as rendering timeline for sites. It also provides critical insight into time to first byte and what could be holding back web page performance
* **[WooRank](https://www.woorank.com/):** WooRank will help you to address issues on your site & identify opportunities to push you ahead of the competition.

### Keywords
* **[Google Trends](https://www.google.com/trends/):** explore Google trending search topics with Google Trends.
* **[Keyword Planner](https://adwords.google.com/KeywordPlanner):** plan your Search Network campaigns and learn what your customers are looking for
* **[Keyword Tool](http://keywordtool.io/):** best FREE alternative to Google Keyword Tool for SEO & PPC keyword research! Get 750+ relevant long-tail keywords from Google Suggest in seconds!
* **[Moz Keyword Explorer](https://moz.com/explorer):** Paid Keyword Tool that provides precise search volume, keyword difficulty, SERP Features and organic click through rate data.

### Links
* **[OpenLinkProfiler](http://www.openlinkprofiler.org/):** get an in-depth analysis of the freshest live backlinks.
* **[Search Engine Spider Simulator](http://tools.seochat.com/tools/search-spider-simulator):** this tool simulates a search engine by displaying the contents of a web page in exactly the way the search engine bot would see it when it crawls the page: See most prominent or inaccessible page elements.
* **[Screaming Frog SEO Spider Tool & Crawler Software](https://www.screamingfrog.co.uk/seo-spider/):** the Screaming Frog SEO Spider is a small desktop program (PC or Mac) which crawls websites’ links, images, CSS, script and apps from an SEO perspective.

### Structured Data
* **[Facebook Debugger](https://developers.facebook.com/tools/debug):** enter the URL you want to scrape to see how the page's markup appears to Facebook
* **[Pinterest](https://developers.pinterest.com/rich_pins/validator/):** validate your Rich Pins and apply to get them on Pinterest
* **[Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/):** paste in your rich snippets or url to test it
* **[Twitter card validator](https://cards-dev.twitter.com/validator):** enter the URL of the page with the meta tags to validate

### Bookmarklets
* **[OuiSEO](https://github.com/carlsednaoui/seo-bookmarklet):** an open-source bookmarklet that shows you on-page SEO and social meta data information.
* **[SEO Bookmarklet](https://twkm.ca/projects/seo-bookmarklet):** a One-Stop SEO Bookmarklet to Quickly Review On-Site SEO

### Browser Extensions
* **[MozBar](https://moz.com/tools/seo-toolbar):** the SEO Toolbar from Moz gives you quick access to many on-page SEO factors, Domain & Page Authority plus a quick nofollow toggle. Download the Free Toolbar today!

### TYPO3 Extensions
* **[Basic SEO Features](https://typo3.org/extensions/repository/view/seo_basics):** Adds a separate field for the title-tag per page, easy and SEO-friendly keywords and description editing in a new module as well as a flexible Google Sitemap.
* **[Google sitemap](https://typo3.org/extensions/repository/view/dd_googlesitemap):** High performance Google sitemap implementation that avoids typical errors by other similar extensions.

## Books
* **[Search engine optimization 2016: Learn SEO with smart internet marketing strategies](https://www.amazon.com/Search-Optimization-Internet-Marketing-Strategies/dp/151534567X):** learn SEO strategies to rank at the top of Google with SEO 2016
* **[Search Engine Optimization All-in-One For Dummies](https://www.amazon.com/Search-Engine-Optimization-All-Dummies/dp/1118921755):** Bruce Clay is one of the most respected figures in the SEO community, teaching classes and workshops at all the major conferences. Like the ‘Art of SEO,’ this book is actually pretty technical and probably not your best easy, first guide, despite being part of the ‘Dummies’ series.
* **[SEO 2016: Learn Search Engine Optimization](https://www.amazon.com/SEO-2016-Search-Engine-Optimization/dp/1512275069):** a Comprehensive Must-Have Guide to SEO in Today's Competitive Search Environment
* **[SEO Fitness Workbook](https://www.amazon.com/SEO-Fitness-Workbook-2016-Optimization/dp/1518748880):** step-by-step book on SEO, starting with goals, going through on page SEO such as page tags, and ending up with off page SEO such as link-building and social mentions.
* **[SEO For Dummies, 6th Edition](http://shop.oreilly.com/product/9781119129554.do):** your fully updated guide to search engine optimization
* **[SEO Step-by-Step - The Complete Beginner's Guide to Getting Traffic from Google](https://www.amazon.com/SEO-Step-Step-Complete-Beginners/dp/1497415020):** also starts with keywords and covers ON PAGE and OFF PAGE SEO. Emphasizes the importance of speed, and has a nice appendix with SEO resources, glossary, and links.
* **[SEO Warrior](http://shop.oreilly.com/product/9780596157081.do):** essential Techniques for Increasing Web Visibility
* **[SEO: Marketing Strategies to Dominate the First Page](https://www.amazon.com/SEO-Marketing-Strategies-analytics-optimization-ebook/dp/B01ACB7LQM):** introduction to Google Analytics, Webmaster, Website traffic, Adwords, Pay per click, Website promotion and Search engine optimization.
* **[The Art of SEO, 3rd Edition](http://shop.oreilly.com/product/0636920032908.do):** mastering search engine optimization
* **[The Beginner's Guide to SEO](https://moz.com/beginners-guide-to-seo):** new to SEO? Need to polish up your knowledge? The Beginner's Guide to SEO has been read over 3 million times and provides the information you need to get on the road to professional quality SEO.
* **[The SEO Battlefield](http://shop.oreilly.com/product/0636920050964.do):** if you want to establish an ongoing SEO program with the goal of increased traffic and search prominence, this practical step-by-step guide will help you understand SEO methodology and then show you how to put those theories into practice.

Reference: netlify.com
