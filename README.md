Faux
===

Faux is a Javascript library for building [Single Page Interface][spi] (or "SPI") applications with [Backbone.js][b]'s Model, View, and Controller classes.

**what's a single page application?**

*Single Page Interface applications are much more responsive than traditional server-side client applications*. Traditional applications fetch a complete page from the server as part of every interaction. The HTTP model and the architecture of browsers imposes a large overhead on every page displayed. SPI applications load one page and thereafter all changes to the page are handled in the browser using Javascript to manipulate the DOM. Interactions with the server are handled in the background using AJAX. The result is a much faster user experience that features a finer-grained, richer model of interaction.

**what is backbone?**

> Backbone supplies structure to JavaScript-heavy applications by providing models with key-value binding and custom events, collections with a rich API of enumerable functions, views with declarative event handling, and connects it all to your existing application over a RESTful JSON interface.--[http://documentcloud.github.com/backbone/](http://documentcloud.github.com/backbone/)

**what is faux?**

Faux is a library that provides *structure* for a backbone application. Backbone provides terrific support for building Model-View-Controller and Proxy-View-Controller applications in Javascript, but Backbone is deliberately agnostic about how to organize your application at an architectural level and how your application should work at a more detailed level.

Faux provides the missing architectural structure: Faux gives you a place to put your templates, a place to put your Javascript, a convention for naming your classes and controller methods, and answers many more questions about how to build an application wit Backbone. And in addition to providing structure for your application, Faux takes advantage of the structure to write a lot of your code for you. That's why if you write:

    controller
      .method('customers');

Faux can wire up a `CustomerCollection` of `Customer` models, connect the collection to a `CustomerCollectionView`, render it through the `customer.haml` template, and connect it to the `#/customers` route. Faux gives you a place to start coding if you're new to Backbone, and a standard set of conventions if you're experienced.

Misadventure
---

Interested in getting a feel for how Faux works? Have a look at our first example application, **Misadvanture**:

<a target="_blank" href="http://min.us/mvkEt6y#1"><img src="http://i.min.us/jeaApo.png" border="0"/></a>

[Misadventure][play] is a little game in the style of [Adventure][a]. Misadventure is written in Javascript and runs entirely in the browser. Misadventure is written in standard Model-View-Controller style, making heavy use of the [Faux][f] and [Backbone.js][b] libraries. Here's a four-part code review:

1. Misadventure, Part I: [Overview][pi]
2. Misadventure, Part II: [controller.wake()][pii]
3. Misadventure, Part III: [Models and Views][piii]
3. Misadventure, Part IV: [Class Loading][piv]

**note**

*Faux was conceived on August 19, 2010 as "Roweis." A remark by Jeremy Ashkenas that we were creating a "Faux Server API" led to its new name.*

*Faux and its documentation is still a work in progress: Future additions to this documentation may or may not include discussions about handling error codes, directly invoking methods, unobtrusive handlers, and some of the other macros such as `title`, `infers`, `redirects_to`, and `location`.*

*Faux was created with the support of the [International Development Research Centre][idrc], a Canadian Crown Corporation created by the Parliament of Canada that supports research in developing countries to promote growth and development. Faux powers software used by the [Think Tank Initiative][tti], a multi-donor program dedicated to strengthening independent policy research institutions—or “think tanks” —in developing countries.*

[aanand]: http://github.com/aanand/
[api]: http://www.joelonsoftware.com/articles/APIWar.html "How Microsoft Lost the API War"
[b]: http://documentcloud.github.com/backbone/
[cloud]: http://getcloudkit.com/
[core]: http://www.ridecore.ca "CORE BMX and Boards"
[couch]: http://couchdb.apache.org/
[cps]: http://en.wikipedia.org/wiki/Continuation-passing_style "Continuation-passing style - Wikipedia, the free encyclopedia"
[c]: /unspace/faux/tree/master/doc/config.md#readme
[functional]: http://osteele.com/sources/javascript/functional/
[f]: /unspace/faux/tree/master/doc/functions.md#readme
[haml]: http://haml-lang.com/ "#haml"
[jamie]: http://github.com/jamiebikies
[k]: https://github.com/raganwald/JQuery-Combinators
[mvp]:  http://github.com/raganwald/homoiconic/blob/master/2010/10/vc_without_m.md#readme "MVC, PVC and (¬M)VC"
[m]: /unspace/faux/tree/master/doc/methods.md#readme
[prg]: http://en.wikipedia.org/wiki/Post/Redirect/Get
[raganwald]: http://github.com/raganwald
[read]: http://weblog.raganwald.com/2007/04/writing-programs-for-people-to-read.html "Writing programs for people to read"
[readme]: /unspace/faux/tree/master/docREADME.md#readme
[sinatra]: http://www.sinatrarb.com/
[spa]: http://en.wikipedia.org/wiki/Single_page_application "Single Page Application"
[spi]: http://itsnat.sourceforge.net/php/spim/spi_manifesto_en.php "The Single Page Interface Manifesto"
[sprout]: http://www.sproutcore.com/
[s]: http://github.com/quirkey/sammy "sammy_js"
[todo]: http://documentcloud.github.com/backbone/examples/todos/index.html
[t]: https://github.com/raganwald/homoiconic/blob/master/2008-10-30/thrush.markdown
[v]: /unspace/faux/tree/master/doc/more_about_views.md#readme
[w]: /unspace/faux/tree/master/doc/writing.md#readme
[wicmajsp]: http://raganwald.posterous.com/why-i-call-myself-a-javascript-programmer "Why I Call Myself a Javascript Programmer"
[idrc]: http://publicwebsite.idrc.ca/
[tti]: http://publicwebsite.idrc.ca/EN/Programs/Social_and_Economic_Policy/Think_Tank_Initiative/Pages/default.aspx
[a]: http://www.digitalhumanities.org/dhq/vol/001/2/000009/000009.html
[f]: https://github.com/unspace/faux
[play]: http://unspace.github.com/misadventure/
[source]: http://github.com/unspace/misadventure
[b]: http://documentcloud.github.com/backbone/
[pi]: http://github.com/raganwald/homoiconic/tree/master/2011/01/misadventure_part_i.md#readme
[pii]: http://github.com/raganwald/homoiconic/tree/master/2011/01/misadventure_part_ii.md#readme
[piii]: http://github.com/raganwald/homoiconic/tree/master/2011/01/misadventure_part_iii.md#readme
[piv]: http://github.com/raganwald/homoiconic/tree/master/2011/02/misadventure_part_iv.md#readme