Machine learning is fueling today’s technological marvels such as driver-less cars, space flight, image and speech recognition. However, one Data Science professional would need a large volume of data to build a robust & reliable machine learning model for such business problems.

Data mining or gathering data is a very primitive step in data science life cycle. As per business requirement one may have to gather data from sources like SAP servers , logs , Databases , APIs , online repositories or web.

Web scraping tools can scrape a large volume of data such as text and images in a relatively short time.

Table of Contents:-
What is Web Scraping
Why Web Scraping
How Web Scraping is useful
Introduction of selenium
What is Selenium
Setup & tools
Implementation of Image Web Scrapping using Selenium Python
Web Scrapping also called “Crawling” or “Spidering” is the technique to gather data automatically from an online source usually from website. While Web Scrapping is an easy way to get large volume of data in relatively short time frame, it adds stress to the server where the source.
Web Scraping can be used by companies to scrap the product data for their products and competing products as well to see how it impacts their pricing strategies. Companies can use this data to fix the optimal pricing for their products so that they can obtain maximum revenue.

2. Market Research
Web scraping can be used for market research by companies. High-quality web scraped data obtained in large volumes can be very helpful for companies in analyzing consumer trends and understanding which direction the company should move in the future. 

3. News Monitoring
Web scraping news sites can provide detailed reports on the current news to a company. This is even more essential for companies that are frequently in the news or that depend on daily news for their day-to-day functioning. After all, news reports can make or break a company in a single day!

4. Sentiment Analysis.
MongoDB also supports user-defined indexes on multiple fields. The order of fields listed in a compound index has significance. For instance, if a compound index consists of {"education": 1, "password": -1 }, the index sorts first by education  and then, within each education value, sort by password. Consider the following illustration of this compound index:

db.userdetails.find().sort({"education":1,"password":-1})
Multikey Index
MongoDB uses multikey indexes to index the content stored in arrays. When you index on a column that holds an array value, MongoDB creates separate index entries for every element of the array. These multikey indexes allow queries to select documents that contain arrays by matching on element or elements of the arrays.

Here is a sample document within a collection :

{
        "_id" : ObjectId("528f34950fe5e6467e58ae77"),
        "user_id" : "user1",
        "password" : "1a2b3c",
        "sex" : "Male",
        "age" : 17,
        "date_of_join" : "16/10/2010",
        "education" : "M.C.A.",
        "profession" : "CONSULTANT",
        "interest" : "MUSIC",
        "extra" : {
                <span class="style1">"friends"</span> : {
                        "<span class="style2">valued_friends_id</span>" : [
                                "kumar",
                                "harry",
                                "anand"
                        ],
                        <span class="style2">"ban_friends_id</span>" : [
                                "Amir",
                                "Raja",
                                "mont"
                        ]
                }
        }
}
We divide modifiers into two groups:

Access Modifiers - controls the access level
Non-Access Modifiers - do not control access level, but provides other functionality
Access Modifiers
For classes, you can use either public or default:

Modifier	Description	Try it
public	The class is accessible by any other class	
default	The class is only accessible by classes in the same package. This is used when you don't specify a modifier. You will learn more about packages in the Packages chapter	
For attributes, methods and constructors, you can use the one of the following:

Modifier	Description	Try it
public	The code is accessible for all classes	
private	The code is only accessible within the declared class	
default	The code is only accessible in the same package. This is used when you don't specify a modifier. You will learn more about packages in the Packages chapter	
protected	The code is accessible in the same package and subclasses. You will learn more about subclasses and superclasses in the Inheritance chapter	
Non-Access Modifiers
For classes, you can use either final or abstract:

Modifier	Description	Try it
final	The class cannot be inherited by other classes (You will learn more about inheritance in the Inheritance chapter)	
abstract	The class cannot be used to create objects (To access an abstract class, it must be inherited from another class. You will learn more about inheritance and abstraction in the Inheritance and Abstraction chapters)	
For attributes and methods, you can use the one of the following:

Modifier	Description
final	Attributes and methods cannot be overridden/modified
static	Attributes and methods belongs to the class, rather than an object
abstract	Can only be used in an abstract class, and can only be used on methods. The method does not have a body, for example abstract void run();. The body is provided by the subclass (inherited from).
An important consideration with the Aggregation Framework is that an index can only be used to fetch the initial data for a pipeline (e.g. usage of $match, $sort, $geonear at the beginning of a pipeline) as well as subsequent $lookup and $graphLookup stages. Once data has been fetched into the aggregation pipeline for processing (e.g. passing through stages like $project, $unwind, and $group) further manipulation will be in-memory (possibly using temporary files if the allowDiskUse option is set).

Optimizing pipelines
In general, you can optimize aggregation pipelines by:

Starting a pipeline with a $match stage to restrict processing to relevant documents.
Ensuring the initial $match / $sort stages are supported by an efficient index.
Filtering data early using $match, $limit , and $skip .
Minimizing unnecessary stages and document manipulation (perhaps reconsidering your schema if complicated aggregation gymnastics are required).
Taking advantage of newer aggregation operators if you have upgraded your MongoDB server. For example, MongoDB 3.4 added many new aggregation stages and expressions including support for working with arrays, strings, and facets.
There are also a number of Aggregation Pipeline Optimizations that automatically happen depending on your MongoDB server version. For example, adjacent stages may be coalesced and/or reordered to improve execution without affecting the output results.

Limitations
As at MongoDB 3.4, the Aggregation Framework explain option provides information on how a pipeline is processed but does not support the same level of detail as the executionStats mode for a find() query. If you are focused on optimizing initial query execution you will likely find it beneficial to review the equivalent find().explain() query with executionStats or allPlansExecution verbosity.

There are a few relevant feature requests to watch/upvote in the MongoDB issue tracker regarding more detailed execution stats to help optimize/profile aggregation pipelines:

SERVER-19758: Add "executionStats" and "allPlansExecution" explain modes to aggregation explain
SERVER-21784: Track execution stats for each aggregation pipeline stage and expose via explain
SERVER-22622: Improve $lookup explain to indicate query plan on the "from" collection

Starting with version 2.6.x mongodb allows users to do explain with aggregation framework.

All you need to do is to add explain : true


