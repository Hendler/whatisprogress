---
title: 'Soliciting Advice: highly concurrent, available, non-blocking server'
author: hendler
type: post
date: 2010-03-26T22:32:00+00:00
excerpt: "I'm seeking feedback on a language or platform for a highly reliable and low latency web service / application. Assumption Bottlenecks in a web service are usually related to data retrieval and storage, and eventually bandwidth and latency. Highly..."
url: /?p=10
categories:
  - Uncategorized
tags:
  - concurrency
  - java
  - nodejs
  - python
  - scala
  - scalability

---
<div>
  I&#8217;m seeking feedback on a language or platform for a highly reliable and low latency web service / application.
</div>

<div>
  <strong>Assumption</strong>
</div>

<div>
  Bottlenecks in a web service are usually related to data retrieval and storage, and eventually bandwidth and latency.&nbsp;
</div>

<div>
  Highly concurrent, lightweight threads provide options for reliability, load distribution, and perceived performance that would otherwise not be available.&nbsp;
</div>

<div>
  <strong>General Requirements&nbsp;</strong>
</div>

<div>
  <ul class="MailOutline">
    <li>
      Easy to use (build, deploy, monitor)
    </li>
    <li>
      Plentiful external, stable, pre-integrated Libraries
    </li>
    <li>
      Use case: distributed, non-blocking web services
    </li>
    <li>
      Quite a bit of message and job queueing&nbsp;
    </li>
    <li>
      multiple databases , caching
    </li>
  </ul>
</div>

<div>
  <strong>Top candidates</strong>
</div>

<div>
  Very incomplete list of pros and cons, but some of my thoughts, highlighted.&nbsp;
</div>

<div>
  <ul class="MailOutline">
    <li>
      <strong><em><a href="http://www.scala-lang.org/">Scala</a></em></strong> <ul>
        <li>
          pros <ul>
            <li>
              assume it will take great advantage of Java 1.7 concurrency, multi-core
            </li>
            <li>
              fairly trivial import of external java libs (except for non-thread safe?) <ul>
                <li>
                  e.g. ZooKeeper &#8211; <a href="http://hadoop.apache.org/zookeeper/docs/r3.0.0/index.html">http://hadoop.apache.org/zookeeper/docs/r3.0.0/index.html</a>
                </li>
              </ul>
            </li>
          </ul>
        </li>
        
        <li>
          cons <ul>
            <li>
              new language syntax, paradigm learning curve
            </li>
            <li>
              doubts about JVM memory efficiency and stability as resources are constrained
            </li>
          </ul>
        </li>
      </ul>
    </li>
    
    <li>
      <strong><em>Server Side Javascript</em></strong> &#8211; via&nbsp;<a href="http://nodejs.org/"> node.js</a>&nbsp;&nbsp; <ul>
        <li>
          pros <ul>
            <li>
              redis integration for caching
            </li>
            <li>
              fast, lightweight, easy language.&nbsp;
            </li>
            <li>
              some custom js would be portable to browsers (coolness)
            </li>
          </ul>
        </li>
        
        <li>
          cons <ul>
            <li>
              very new
            </li>
            <li>
              performance
            </li>
            <li>
              not as many external libs?
            </li>
          </ul>
        </li>
      </ul>
    </li>
    
    <li>
      <a href="http://www.tornadoweb.org/">Tornado</a> <ul>
        <li>
          pros <ul>
            <li>
              Python <ul>
                <li>
                  as many libs as Scala
                </li>
              </ul>
            </li>
          </ul>
        </li>
        
        <li>
          cons <ul>
            <li>
              narrower use cases
            </li>
            <li>
              performance
            </li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</div>

<div>
  &nbsp;Would love comments, but a more complete list is presented in a survey:
</div>

<div>
  <div>
    <span class="Apple-tab-span"> </span><a href="http://www.surveymonkey.com/s/ZGQP6YJ" target="_blank">http://www.surveymonkey.com/s/ZGQP6YJ</a>
  </div>
</div>