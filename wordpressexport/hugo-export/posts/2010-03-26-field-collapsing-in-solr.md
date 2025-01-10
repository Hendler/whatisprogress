---
title: Field Collapsing in SOLR
author: hendler
type: post
date: 2010-03-26T19:34:00+00:00
excerpt: Field Collapsing Field collapsing allows something akin to a "group by" in SOLR, so that the number of results returned reflect a logical grouping rather than another total. Faceting can be used in conjunction. Facet counts reflect subsets within ...
url: /?p=5
categories:
  - Uncategorized
tags:
  - java
  - search
  - solr

---
<div>
  <span style="font-weight:bold;">Field Collapsing</span>
</div>

<div>
</div>

<div>
  <a href="http://wiki.apache.org/solr/FieldCollapsing" target="_blank">Field collapsing</a> allows something akin to a &#8220;group by&#8221; in <a href="http://lucene.apache.org/solr/" target="_blank">SOLR</a>, so that the number of results returned reflect a logical grouping rather than another total.??
</div>

<div>
  Faceting can be used in conjunction. Facet counts reflect subsets within results, where-as collapse counts are <em>group by</em> counts.
</div>

<div>
</div>

<div>
  This means that Field Collapsing could be used for certain analytics, as well as the common use-case of nesting and grouping results. To use effectively, I found it helpful to &#8220;pre-collapse&#8221; certain fields, so that a new, unique string was created that could be used to easily group, since I believe you can only field collapse on a single field. (If I&#8217;m wrong, please let me know!)
</div>

<div>
</div>

<div>
  <strong>Special Setup</strong>
</div>

<div>
</div>

<div>
  This assumes you are or will be running a development version of SOLR (trunk via SVN).
</div>

<div>
  Field collapsing is not yet available in SOLR trunk and you must apply a patch file to SOLR and build again.
</div>

<div>
  If pulling in from trunk, download the patch found at <a href="https://issues.apache.org/jira/browse/SOLR-236">https://issues.apache.org/jira/browse/SOLR-236</a> in to your solr source code directory.
</div>

_wget <https://issues.apache.org/jira/secure/attachment/12440108/SOLR-236-trunk.patch>  
patch -p 1 -i SOLR-236-trunk.patch_

<div>
  And rebuild using supplied Apache Ant scripts.
</div>

<div>
</div>

<div>
  Read more on these sites or in the comprehensive &#8220;<a href="http://www.packtpub.com/solr-1-4-enterprise-search-server/book" target="_blank">Solr 1.4, Enterprise Search Server</a>&#8221; page 191.
</div>

<div>
  <div>
    <a href="http://wiki.apache.org/solr/FieldCollapsing">http://wiki.apache.org/solr/FieldCollapsing</a>
  </div>
  
  <div>
    <a href="http://blog.jteam.nl/2009/10/20/result-grouping-field-collapsing-with-solr/">http://blog.jteam.nl/2009/10/20/result-grouping-field-collapsing-with-solr/</a>
  </div>
</div>

<div>
</div>

<div>
  <div>
    <strong>Why SOLR</strong>
  </div>
  
  <div>
  </div>
  
  <div>
    SOLR has a been a great tool for <a href="http://BetterLesson.org">BetterLesson.org</a>. Because our primary database is MySQL, we looked at around 8 full-text indexers &#8211; but the two finalists were Sphinx [1] and SOLR. Sphinx had very tight integration with MySQL, so the learning curve seemed less. ??SOLR required a JVM, an app server, and quite a lot of configuration.
  </div>
  
  <div>
  </div>
  
  <div>
    When we were deciding, an <a href="http://www.packtpub.com/solr-1-4-enterprise-search-server/book" target="_blank">excellent SOLR book</a> came out just when we were choosing. Further the SOLR IRC channel and mailing list for SOLR are friendly and quite active. We even had the option for commercial support through Massachusetts&#8217; own Lucid Imagination. So I dove in.??While the configuration is non-trivial, but the configuration parameters have proven very powerful.??
  </div>
  
  <div>
  </div>
  
  <div>
    <strong>More background:</strong>
  </div>
  
  <div>
  </div>
  
  <div>
    I had written a half-dozen or so custom faceted search interfaces &#8211; almost entirely using MySQL, and even one used <a href="http://www.openrdf.org/" target="_blank">Sesame</a> (an RDF store &#8211; and it eventually worked pretty well). Skipping the stories of pain, confusion and suffering on the road to enlightenment &#8211; SOLR has been great.??Used extensively at <a href="http://Netflix.com">Netflix.com</a>, <a href="http://Zappos.com">Zappos.com</a>, <a href="http://CitySearch.com">CitySearch.com</a>, <a href="http://Reddit.com">Reddit.com</a>, <a href="http://Wego.com">Wego.com</a>, <a href="http://Whitehouse.gov">Whitehouse.gov</a>, <a href="http://Drupalgardens.com">Drupalgardens.com</a> and others [2], ??supported by Apache, based on Lucene, SOLR provides a scalable, distributed search and has good data import from MySQL, including delta queries.
  </div>
</div>

<div>
</div>

<div>
  [1] &#8211; Sphinx is used by Craigslist and <a href="http://www.sphinxsearch.com/powered.html">http://www.sphinxsearch.com/powered.html</a>
</div>

<div>
  [2] &#8211; <a href="http://wiki.apache.org/solr/PublicServers">http://wiki.apache.org/solr/PublicServers</a>
</div>