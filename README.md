[Apache Lucene](https://lucene.apache.org/) is an outstanding [information retrieval](https://en.wikipedia.org/wiki/Information_retrieval) system built on the Java runtime. There is a .Net alternative but the [Lucene.Net](https://lucenenet.apache.org/) team are to this date three major versions behind the Java team. Also, the Lucene code base is big and complex and difficult to understand. This is a great opportunity to build a new information retrieval system.

# Resin

Resin is a modern information retrieval system, a document based search engine library and framework, and a Lucene clone.

## Documentation

##Say you have a document.

	{
		"_id": "Q1",
		"label":  "universe",
		"description": "totality of planets, stars, galaxies, intergalactic space, or all matter or all energy",
		"aliases": "cosmos The Universe existence space outerspace"
	}

##Wait, say you have a huge number documents.
	
	var docs = GetWikipediaAsJson();

##Add them to a Resin index

	var dir = @"C:\Users\Yourname\Resin\wikipedia";
	using (var writer = new IndexWriter(dir, new Analyzer()))
	{
		writer.Write(docs);
	}

##Query the index
<a name="inproc" id="inproc"></a>

	var searcher = new Searcher(dir);
	var result = searcher.Search("description:matter or energy");

[More here](https://github.com/kreeben/resin/wiki). 

## Contribute

Here are some [issues](https://github.com/kreeben/resin/issues) that need to be sorted.

Pull requests are accepted.

## Power to the people

Great knowledge about IR can be found with the big tech corporations of today, Google, Microsoft, Facebook. It is undemocratic that people can reach the information available on the internet solely through the means of services that these corporations offer.

Even if the internet's data is available to all, because it is so vast it can't be properly digested by humans unless a machine first makes sense of it. Google, Microsoft and Facebook have great machines. We should to.

IR is perhaps the smallest and most fundemental component of AI.

AI should empower us all. It should not be monopolized by corporations. It should be free.

Peace

## Sir

[Sir](https://github.com/kreeben/sir) is an Elasticsearch clone built on Resin.
