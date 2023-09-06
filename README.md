<p>
<image src="Afbeelding1.jpg" hspace="10"/>
<image src="KB_Nationale-Bibliotheek_Logo_RGB-Zwart-EN.jpg" width="400" align="top"/>
</p>
		
# Wikibase resources
*A collection of resources, overviews, links and knowlegde related to Wikibase, collected and curated by KB, national library of the Netherlands.*

**Work in progress!!**

This overview was originally extracted from the slides of the lecture *Introduction Wikibase, the basics*, for employeees of [KB, national library of the Netherlands](https://www.kb.nl) on 7 September 2023. This slidedeck is availble on [Wikimedia Commons]() and [Zendo]()

This overview is heavily inspired by the *[Wikibase knowledge graphs, A collection of open source tools and resources related to Wikibase knowledge graphs](https://github.com/shigapov/wikibase-knowledge-graphs)* by Renat Shigapov. I've used this overview many times to improve my understanding of the Wikibase universe, and hope to extend it via the overview below, and help others in a similar way.

This page is maintained by Olaf Janssen, Wikimedia coordinator of KB. See his [Wikidata user page](https://www.wikidata.org/wiki/User:OlafJanssen) and [expert page on kb.nl](https://www.kb.nl/over-ons/experts/olaf-janssen) for contact details.

Latest update: 6 September 2023
<hr>

### Contents
  * [Requesting data from a Wikibase](#requesting-data-from-a-Wikibase)
  * [Adding data to a Wikibase](#adding-data-to-a-Wikibase)
  * [Wikibase community](#wikibase-community)
  * [Staying updated](#staying-updated)
  * [Finding help](#finding-help)
<hr>

[History of Wikibase](https://addshore.com/2022/02/wikibase-a-history/) (until Febr 2022) ([archived version](https://web.archive.org/web/20230714110136/https://addshore.com/2022/02/wikibase-a-history/))

### Requesting data from a Wikibase 

#### 1) HTML content in web browser
*Theun de Vries* in KB sandbox Wikibase GUI, 4 equivalent URLs
* https://kbtestwikibase.wikibase.cloud/entity/Q29
* https://kbtestwikibase.wikibase.cloud/wiki/Item:Q29
* https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29
* https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData?id=Q29&format=html

#### 2) Non-HTML content in web browser
* JSON: [Special:EntityData/Q29.json](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29.json) or [Special:EntityData?id=Q29&format=json](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData?id=Q29&format=json)
* RDF/XML: [Special:EntityData/Q29.rdf](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29.rdf) or [Special:EntityData?id=Q29&format=rdf](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData?id=Q29&format=rdf)  
* Other formats: [Q29.jsonld](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29.jsonld), [Q29.ttl](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29.ttl), [Q29.n3](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29.n3), [Q29.nt](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29.nt) and [Q29.php](https://kbtestwikibase.wikibase.cloud/wiki/Special:EntityData/Q29.php) 

#### 3) MediaWiki Action API
* General API for all Wikimedia projects (Wikidata, Wikipedia, Wikimedia Commons etc.)
* API endpoint for KB sandbox WB: https://kbtestwikibase.wikibase.cloud/w/api.php
* [wbgetentities](https://kbtestwikibase.wikibase.cloud/w/api.php?action=help&modules=wbgetentities) and [wbgetclaims](https://kbtestwikibase.wikibase.cloud/w/api.php?action=help&modules=wbgetclaims) modules for requesting data
* Q29 as JSON:  https://kbtestwikibase.wikibase.cloud/w/api.php?action=wbgetentities&ids=Q29&format=json
* Q29 as XML: https://kbtestwikibase.wikibase.cloud/w/api.php?action=wbgetentities&ids=Q29&format=xml 

#### 4) SPARQL
* FactGrid: [Living addresses of Parisian painters in 1834](https://tinyurl.com/2mrnynpd)
* FactGrid: [Ages of deceased persons](https://tinyurl.com/2y6f78x5)
* EU Knowlegde Graph: [Buildings of the EU](https://tinyurl.com/242a3rrh) 
* KB Wikibase: [Medieval manuscripts of the KB](https://tinyurl.com/2bxb8hkn )  

<hr>

### Adding data to a Wikibase 
Useful links: 
* https://www.mediawiki.org/wiki/Wikibase/Importing
* https://github.com/shigapov/wikibase-knowledge-graphs#data-import
* https://www.wikibase.consulting/fast-bulk-import-into-wikibase/ 

#### 1) Add a new item via the GUI
Using [KB's sandbox WB](https://kbtestwikibase.wikibase.cloud/wiki/Main_Page) (if logged in) we can create a [NewItem](https://kbtestwikibase.wikibase.cloud/wiki/Special:NewItem), resulting into an item about the Dutch poet [H.H. ter Balkt](https://kbtestwikibase.wikibase.cloud/wiki/Item:Q32)  

#### 2) OpenRefine (in bulk)
* OpenRefine is a well-known tool for editing, enriching and manipulating data. It is widely used to add data to Wikidata and other Wikibase instances.
* OpenRefine-Wikidata workshop, KB, 4-7-2023: [](https://github.com/KBNLwikimedia/OpenRefine-Introduction-Workshop) + (https://zenodo.org/record/8207914)
* Winnaars Halewijn literatuurprijs-
* Scenario 1 : We willen kijken of deze namen in bepaalde Wikibases voorkomen (reconciliatie). Reconciliatie API endpoints of [Wikidata](), [FactGrid](), [Kunstmuseum]() en [KB]()
* Scenario 2: We willen (nieuwe, verrijkte, verbeterde) data wegschrijven in (bv.) de KB Wikibase - Koppel OpenRefine aan de KB-Wikibase. OpenRefine manifests (json) of [Wikidata](), [FactGrid](), [Kunstmuseum]() en [KB]()
* 
* Hoe werken deze scenario's precies? - https://en.wikiversity.org/wiki/OpenRefine_to_Wikibase:_Data_Upload_Pipeline- https://docs.openrefine.org/manual/wikibase/configuration + https://docs.openrefine.org/manual/wikibase/reconciling + https://openrefine.org/docs/manual/wikibase/uploading- https://github.com/KBNLresearch/OpenRefine-Wikibase

#### 3) QuickStatements (in bulk)
* "From formatted .txt or .csv to Wikibase"
* https://meta.wikimedia.org/wiki/QuickStatements + [help](https://www.wikidata.org/wiki/Help:QuickStatements)
* [QuickStatements interface in KB sandbox WB](https://kbtestwikibase.wikibase.cloud/tools/quickstatements/#/batch)

#### 4) Advanced data import tools
* [WikibaseImport](https://github.com/Wikidata/WikibaseImport), a MediaWiki extension   
* [WikibaseIntegrator](https://github.com/LeMyst/WikibaseIntegrator), a Python library ([docs](https://pypi.org/project/wikibaseintegrator/0.11.2/))  
* [WikidataIntegrator](https://github.com/SuLab/WikidataIntegrator), a Python library ([Zenodo](https://zenodo.org/record/8004921))  
* [WikibaseSync](https://github.com/the-qa-company/WikibaseSync), a Python library ([Tutorial](https://wikibase.the-qa-company.com/wiki/WikibaseSync_-_Tutorial)) 
* [wikibase-edit](https://github.com/maxlath/wikibase-edit), a NodeJS library ([Howto](https://github.com/maxlath/wikibase-edit/blob/master/docs/how_to.md)) 
* [wikibase-cli](https://github.com/maxlath/wikibase-cli), a command-line interface   
* [VanDerBot](https://heardlibrary.github.io/digital-scholarship/lod/wikibase/load/), a Python application ([Github](https://github.com/HeardLibrary/linked-data/tree/master/vanderbot)) 
* [Pywikibot](https://www.mediawiki.org/wiki/Manual:Pywikibot), a Python library ([Github](https://github.com/wikimedia/pywikibot), [Wikibase scripts](https://doc.wikimedia.org/pywikibot/stable/scripts/wikibase.html))  
* [RaiseWikibase](https://github.com/UB-Mannheim/RaiseWikibase), a Python tool 
* [Wikidata-Toolkit](https://www.mediawiki.org/wiki/Wikidata_Toolkit), a Java library ([Github](https://github.com/Wikidata/Wikidata-Toolkit))  

<hr>

### Wikibase community
#### 1) Wikibase Community User Group (WBCUG)
*Its mission is to cultivate Wikibase's development and to encourage like-minded developers and data analysts not only to improve Wikibase's existing tools but also to create new ones.* 

[About the WBCUG](https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group) - [WBCUG history](https://www.lehir.net/a-short-history-of-the-wikibase-community-user-group/) - [WBCUG members](https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group) - [WBCUG monthly online meetings - The Wikibase Live sessions](https://meta.wikimedia.org/wiki/Category:Wikibase_Community_User_Group/Meetings) - [WBCUG Mailing list](https://lists.wikimedia.org/postorius/lists/wikibaseug.lists.wikimedia.org) - [WBCUG Telegram](https://t.me/+WBsf9-C9KPuMZCDT) (or [here](https://t.me/joinchat/HGjGexZ9NE7BwpXzMsoDLA))  
	
#### 2) Wikibase Stakeholder Group (WBSG)
*Commissions production and maintenance of open source extensions to Wikibase, and documentation for institutions that want to operate and maintain a fully-fledged instance of Wikibase. The group will focus on extensions to Wikibase instead of contributing to Wikibase core.*

[About the WBSG](https://wbstakeholder.group/about) - [WBSG members](https://wbstakeholder.group/members) - [WBSG monthly online meeting minutes](https://notepad.rhizome.org/wikibase-stakeholder-meetings#) - [WBSG Loomio](https://loomio.rhizome.org/wbsg/) - [WBSG Mastodon](https://mastodon.social/web/@wbstakeholders) - [WBSG Twitter](https://twitter.com/wbstakeholders)

#### 3) Wikibase Knowlegde Group Netherlands (WBGNL)
*The aim of this group is to bundle and exchange knowledge & experiences about the use of Wikibase, to learn from each other, and to keep each other informed about the (international) developments and opportunities surrounding Wikibase. Membership is open to everyone in the Netherlands who already works with Wikibase, wants to work with, or is otherwise interested in this software. Mainly for - but certainly not limited to - professionals from Dutch heritage and knowledge institutions, and related organizations and companies.*  

[About the WBGNL](https://www.wikidata.org/wiki/Wikidata:GLAM/Koninklijke_Bibliotheek_Nederland/WikibaseActivities#Dutch_Wikibase_knowledge_group) - [WBGNL meetings](https://wbstakeholder.group/events/presentations#netherlands-wikibase-knowledge-group) (also available [here](https://www.wikidata.org/wiki/Wikidata:GLAM/Koninklijke_Bibliotheek_Nederland/WikibaseActivities#Meetings)) - [WBGNL mailing list](https://lists.wmnederland.nl/mailman/listinfo/wikibase-nl) - [WBGNL Loomio](https://loomio.rhizome.org/wbgn/)

#### 4) Wikibase community workshops, trainings, meetups etc.
* [The first Federated-Wikibase-Workshop: Antwerp](https://www.wikidata.org/wiki/Wikidata:WikiProject_Wikidata_for_research/Meetups/2018-04-23-25-Antwerpen), April 2018 ([blog](https://blog.factgrid.de/archives/835))
* [Wikibase Workshop in Berlin](https://www.wikidata.org/wiki/Wikidata:WikiProject_Wikidata_for_research/Meetups/2018-06-17-19-Berlin), June 2018 ([blog](https://blog.wikimedia.de/2018/07/13/wikibase-workshop-in-berlin/))
* [The Wikibase Summit: New York](https://www.wikidata.org/wiki/Wikidata:WikiProject_Wikidata_for_research/Meetups/2018-09-19-21-New-York), September 2018
* [Ghent University Wikidata and Wikibase Workshop: developing a Wikibase instance](https://www.wikidata.org/wiki/Wikidata:Events/Belgium/Universiteit_Gent/Wikidata_and_Wikibase_Workshop/2019),  July 2019 
* [Wikidata & Wikibase for National Libraries: the inaugural meeting](https://pro.europeana.eu/post/wikidata-wikibase-for-national-libraries-the-inaugural-meeting), Stockholm, August 2019
* [Wikibase workshop in Tokyo ](https://twitter.com/andrawaag/status/1178496977723543552), September 2019
* [Wikibase in Knowledge Graph based Research Data Management (NFDI) Projects](https://nfdi4culture.de/events/1-wikibase-workshop.html), online, 23 February 2021 ([report](https://nfdi4culture.de/news/wikibase-workshop.html))
* [JCDL workshop: Open Refine to Wikibase - A New Data Upload Pipeline](https://nfdi4culture.de/events/jcdl-workshop-open-refine-to-wikibase-a-new-data-upload-pipeline), June 2022
* [First SEMIC workshop on Wikidata and Wikibase](https://joinup.ec.europa.eu/collection/semic-support-centre/event/first-workshop-wikidata-and-wikibase), online, 24 January 2023
* [Second SEMIC workshop on Wikidata and Wikibase](https://joinup.ec.europa.eu/collection/semic-support-centre/event/second-workshop-wikidata-and-wikibase), Brussel, 23 February 2023 
* [Third SEMIC workshop on Wikidata and Wikibase](https://joinup.ec.europa.eu/collection/semic-support-centre/event/third-workshop-wikidata-and-wikibase), online, 28 March 2023
* [First Wikibase lexical data workshop](https://wikibase-lex.sciencesconf.org/), Wenen, Septemer 2023  
<hr>

### Staying updated
* Via de meetings, notulen, presentaties, mailinglijsten, socials etc. van de WBCUG, WBSG en WBGNL. – zie overzicht hiervoor.
* Wikibase.cloud: - Project updates Wikibase.cloud: https://meta.wikimedia.org/wiki/Wikibase/Wikibase.cloud- Mailing list Wikibase.cloud:  https://lists.wikimedia.org/postorius/lists/wikibase-cloud.lists.wikimedia.org
* Specifiek voor bibliotheken:- Wikibase Working Hours - Community discussion of Wikidata & Wikibase with the goal of understanding how the library can contribute to and leverage these as a platform for publishing, linking, and enriching library linked data - https://www.wikidata.org/wiki/Wikidata:WikiProject_LD4_Wikidata_Affinity_Group/Wikibase_Working_Hours- IFLA Wikidata Working Group - This working group will explore and advocate for the use of and contribution to Wikidata by library and information professionals, the integration of Wikidata and Wikibase with library systems, and alignment of the Wikidata ontology with library metadata formats such as BIBFRAME, RDA, and MARC - https://mail.iflalists.org/wws/info/wikidatawg  
* More: Wikidata Weekly Summary, bevat ook WB updates! https://www.wikidata.org/wiki/Wikidata:Status_updates  + https://www.wikidata.org/wiki/Topic:Xks1m3byqvkjdhz1  +  https://www.wikidata.org/wiki/Wikidata:Status_updates/2023_06_26- Wikibase yearly summaries (Envel Le Hir): https://www.lehir.net/wikibase-yearly-summary-2022/ (2021, 2020)- Blog Addshore, over Wikibase: https://addshore.com/?s=wikibase 

<hr>

### Finding help
#### Active help (by humans) 
* Help by community: use all community channels above.
* Tip: Use the Telegram channels if you want help quickly
* Help by Olaf Janssen: [Wikidata user page](https://www.wikidata.org/wiki/User:OlafJanssen) + [Expert page on kb.nl](https://www.kb.nl/over-ons/experts/olaf-janssen)   

#### Passive help (documentation, manuals, HOWTOs, tutorials etc). 
* Wikibase documentatie portal (WMDE): https://www.mediawiki.org/wiki/Wikibase + https://www.mediawiki.org/wiki/Wikibase/Using_Wikibase  
* Wikibase technische documentatie (low-level): https://doc.wikimedia.org/Wikibase/master/php
* Wikibase.cloud documentation portal (WMDE):  https://www.mediawiki.org/wiki/Wikibase/Wikibase.cloud + https://phabricator.wikimedia.org/tag/wikibase.cloud/ (WB.cloud issue tracker)

#### More help
* [Learning Wikibase](https://learningwikibase.com), a place to learn and share online resources (e.g. articles, videos, workflows, FAQ’s) that make it easier to install, maintain or customize your Wikibase instance. - 
* Tip!! [Wikibase resources overview](https://github.com/shigapov/wikibase-knowledge-graphs) by Renat Shigapov 
* [UCLA Library Research Guide on Wikibase and Wikidata](https://guides.library.ucla.edu/semantic-web/wikidata#s-lg-page-section-6895500)  
* [Awesome Wikibase tutorials](https://github.com/shigapov/wikibase-knowledge-graphs#awesome-wikibase-tutorials) collected by Renat Shigapov. 
 


