---
title: Startups are built with both Undone and Unsung Engineering
author: hendler
type: post
date: 2010-05-13T18:06:00+00:00
excerpt: For me, web engineers are the magicians behind the curtain. That can mean not-a-lot of glory. But for engineers like myself, undone engineering is more painful than unsung engineering. One of the most difficult aspects of being a good engineer is ...
url: /?p=8
categories:
  - Uncategorized

---
<div>
  For me, web engineers are the magicians behind the curtain. That can mean not-a-lot of glory.
</div>

<div>
  But for engineers like myself, undone engineering is more painful than unsung engineering.??One of the most difficult aspects of being a good engineer is knowing when to sacrifice good engineering. ??Startups, are by definition, challenging the established way of doing business, so the established way of doing great engineering sometimes isn&#8217;t good enough to survive. ??
</div>

<div>
  <em>( Although this is a topic pretty well covered in writing about startups , I try translate the constraints of a startup into what a priority list for technical leadership might look like. )??</em>
</div>

<div>
  Everything in a startup changes fast.??Engineering is managed chaos.??There are new team members, new customers, new data, new open source libraries, etc. Good engineering can accommodate change, but usually change is unexpected. As a side effect, the non-technical team begins to depend on the shortcuts, and the shortcuts begin to show their weaknesses. The design team has new ideas, and you can&#8217;t say yes as often as you used to.??
</div>

<div>
  But you survive.??
</div>

<div>
  Here are the priorities I use to keep everything moving for a web application startup (follows an 80 / 20 rule pretty well):
</div>

<div>
  <ol class="MailOutline">
    <li>
      <strong>protect the data (files/database, etc)</strong> <ol>
        <li>
          back it up
        </li>
        <li>
          make sure data is valid (ideally some smoke tests, unit tests, regression tests on the data layer of an application)
        </li>
        <li>
          back it up
        </li>
        <li>
          source control with easy to understand policies and branching
        </li>
        <li>
          back it up
        </li>
        <li>
          automate backing it up
        </li>
      </ol>
    </li>
    
    <li>
      <strong>fix problems with the user experiences</strong> <ol>
        <li>
          small visual problems can make people &#8230; disgusted. Fonts, cross browser issues take a lot of time, but matter to people who expect things to work.??
        </li>
        <li>
          client (browser) speed &#8211; a small javascript issue can cause a page load to appear to take 5 seconds. <em>Perceived</em> performance is all that matters.??
        </li>
        <li>
          fix display issues &#8211; if they think data is lost, then it is??
        </li>
        <li>
          integrated QA team &#8211; make everyone on the team test the site, but not their own work.
        </li>
      </ol>
    </li>
    
    <li>
      <strong>make coding fast</strong> <ol>
        <li>
          establish team communication that makes product iteration rapid
        </li>
        <li>
          use frameworks, existing but stable libraries (open source so you can fix critical problems yourself)
        </li>
        <li>
          keep version control and deployment as automated as possible for the whole team
        </li>
        <li>
          write easy to understand code
        </li>
        <li>
          document code and best practices (wiki style)
        </li>
        <li>
          track problems (bugs and backlogs)
        </li>
        <li>
          write test code (on critical areas)
        </li>
      </ol>
    </li>
    
    <li>
      <strong>housekeeping</strong> <ol>
        <li>
          refactor
        </li>
        <li>
          cleanup
        </li>
        <li>
          more test code
        </li>
      </ol>
    </li>
    
    <li>
      <strong>new features/ scaling/performance</strong>??- probably the most fun for an engineer, but last on the list. This has been the hardest for me. ??Engineers need to think about scaling when the system is architected&#8230;. maybe. But when you have just a 10 customers and the entire database fits in memory&#8230; why worry? <ol>
        <li>
          database ??- a typical bottleneck. NoSQL and distributed architectures are making this easier
        </li>
        <li>
          separate web server from application layer. Concentrate core application logic into languages that are better suited for scaling and concurrency issues
        </li>
        <li>
          load balance, messaging queues, etc
        </li>
      </ol>
    </li>
  </ol>
  
  <p />
  
  <div>
    Because of the list above, not every engineer out of a great tech school or amazing high tech corporation adjusts to startup life well. But when the above begins to pay dividends, engineers appreciate the big picture.
  </div>
  
  <p />
</div>