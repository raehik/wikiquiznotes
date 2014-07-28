[MediaWiki API documentation](http://www.mediawiki.org/wiki/API:Main_page#Introduction)

Our example request:

    http://en.wikipedia.org/w/api.php?format=json&action=query&titles=Heat&prop=revisions&rvprop=content

Now we'll break it down:

    w/api.php

    format=json

    action=query

    titles=Heat

Title of requested page. This is pretty much the only thing we want to change.

    prop=revisions

    rvprop=content



Output:

    {"query":{"pages":{"19593167":{"pageid":19593167,"ns":0,"title":"Heat","revisions":[{"contentformat":"text/x-wiki","contentmodel":"wikitext","*":"{{About|a type of transfer of energy, from a hotter body to a colder one|for other uses}}\n{{Use dmy dates|date=August 2013}}\n{{pp-move|small=yes}}\n\nIn [[physics]], '''heating''' is...

The result is in JSON, but the article text is formatted in HTML/Wiki markup.
That's good for us, because it means most of it is plaintext. Also, [[links]]
are easy to search for, and they might be good targets for "What is?" or
"Who discovered?" questions.
