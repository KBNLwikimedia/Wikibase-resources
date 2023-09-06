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
- [Wikibase resources](#wikibase-resources)
    + [Contents](#contents)
    + [Wikibase hosting](#wikibase-hosting)
    + [Requesting data from a Wikibase](#requesting-data-from-a-wikibase)
      - [1) HTML content in web browser](#1--html-content-in-web-browser)
      - [2) Non-HTML content in web browser](#2--non-html-content-in-web-browser)
      - [3) MediaWiki Action API](#3--mediawiki-action-api)
      - [4) SPARQL](#4--sparql)
    + [Cool Wikibase SPARQL queries](#cool-wikibase-sparql-queries)
    + [Adding data to a Wikibase](#adding-data-to-a-wikibase)
      - [1) Add a new item via the GUI](#1--add-a-new-item-via-the-gui)
      - [2) OpenRefine (in bulk)](#2--openrefine--in-bulk-)
      - [3) QuickStatements (in bulk)](#3--quickstatements--in-bulk-)
      - [4) Advanced data import tools](#4--advanced-data-import-tools)
    + [Wikibase community](#wikibase-community)
      - [1) Wikibase Community User Group (WBCUG)](#1--wikibase-community-user-group--wbcug-)
      - [2) Wikibase Stakeholder Group (WBSG)](#2--wikibase-stakeholder-group--wbsg-)
      - [3) Wikibase Knowlegde Group Netherlands (WBGNL)](#3--wikibase-knowlegde-group-netherlands--wbgnl-)
      - [4) Wikibase community workshops, trainings, meetups etc.](#4--wikibase-community-workshops--trainings--meetups-etc)
    + [Staying updated](#staying-updated)
    + [Finding help](#finding-help)
      - [Active help (by humans)](#active-help--by-humans-)
      - [Passive help (documentation, manuals, HOWTOs, tutorials etc).](#passive-help--documentation--manuals--howtos--tutorials-etc-)
      - [More help](#more-help)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

<hr>

[History of Wikibase](https://addshore.com/2022/02/wikibase-a-history/) (until Febr 2022) ([archived version](https://web.archive.org/web/20230714110136/https://addshore.com/2022/02/wikibase-a-history/))

<hr>

### Wikibase hosting
* [Which Wikibase should I choose?](https://www.mediawiki.org/wiki/Wikibase/Which) 
* [Wikibase Suite](https://www.mediawiki.org/wiki/Wikibase/Suite) and [Wikibase Docker](https://www.mediawiki.org/wiki/Wikibase/Docker) - software that you install and run on your own hardware (typically via Docker). Good for users who want to try out Wikibase on their own hardware and who want to customize their installation. Good for institutions with large datasets.
* [Wikibase.cloud](https://www.wikibase.cloud) (Still in closed beta) - free “Wikibase as a service” platform  to create Wikibases quickly and easily managed and maintained by Wikimedia Deutschland.
  - [KB’s sandbox WB instance on Wikibase.cloud](https://kbtestwikibase.wikibase.cloud/wiki/Main_Page)
  - [KB's experiences and first impressions](https://commons.wikimedia.org/wiki/File:KB_Wikibase.cloud_Unboxing_Experience,_Netherlands_Wikibase_Knowlegde_Group,_22-07-2022.pdf) with unboxing, setting up, configuring and tweaking their Wikibase.cloud instance. ([See also here](https://kbtestwikibase.wikibase.cloud/wiki/Main_Page#Our_Wikibase.cloud_unboxing_experience_and_first_findings))
* [Free Wikibase hosting @ Miraheze](https://meta.miraheze.org/wiki/Miraheze)
* [Commercial hosting & services](https://meta.wikimedia.org/wiki/Wikibase/Consultants_and_Support_Providers) 

<hr>

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
* See [Cool Wikibase SPARQL queries ](#cool-wikibase-sparql-queries)

<hr>

### Cool Wikibase SPARQL queries 
* FactGrid: [Living addresses of Parisian painters in 1834](https://tinyurl.com/2mrnynpd)
* FactGrid: [Ages of deceased persons](https://tinyurl.com/2y6f78x5)
* EU Knowlegde Graph: [Buildings of the EU](https://tinyurl.com/242a3rrh) 
* KB Wikibase: [Medieval manuscripts of the KB](https://tinyurl.com/2bxb8hkn)  
<hr>

### Adding data to a Wikibase 
Useful links: 
* https://www.mediawiki.org/wiki/Wikibase/Importing
* https://github.com/shigapov/wikibase-knowledge-graphs#data-import
* https://www.wikibase.consulting/fast-bulk-import-into-wikibase/ 

#### 1) Add a new item via the GUI
Using [KB's sandbox WB](https://kbtestwikibase.wikibase.cloud/wiki/Main_Page) (login required) we can create a [NewItem](https://kbtestwikibase.wikibase.cloud/wiki/Special:NewItem), resulting into an item about the Dutch poet [H.H. ter Balkt](https://kbtestwikibase.wikibase.cloud/wiki/Item:Q32)  

#### 2) OpenRefine (in bulk)
* OpenRefine is a well-known tool for editing, enriching and manipulating data. It is widely used to add data to Wikidata and other Wikibase instances.
* [OpenRefine-Wikidata introduction workshop](https://github.com/KBNLwikimedia/OpenRefine-Introduction-Workshop), KB, 4-7-2023 (also on [Zenodo](https://zenodo.org/record/8207914))
* Documentation: [Connecting OpenRefine to a Wikibase instance](https://docs.openrefine.org/manual/wikibase/configuration), [Reconciling with Wikibase](https://docs.openrefine.org/manual/wikibase/reconciling) and [Uploading edits to Wikibase](https://openrefine.org/docs/manual/wikibase/uploading)
* Wikibase reconcilation services: [Wikidata](https://wikidata.reconci.link/en/api), [FactGrid](https://database.factgrid.de/reconcile/en/api), [Kunstmuseum](https://reconciliation.kunstmuseum.nl/nl/api) and [more](https://reconciliation-api.github.io/testbench/#/)
* Connecting OpenRefine to a Wikibase via a manifests.json file: [Wikidata](https://raw.githubusercontent.com/OpenRefine/wikibase-manifests/master/wikidata-manifest.json), [FactGrid](https://github.com/OpenRefine/wikibase-manifests/blob/master/factgrid-manifest.json), [Kunstmuseum](https://api.kunstmuseum.nl/wiki/Kunstmuseum_API#Reconciliation) and [more](https://github.com/OpenRefine/wikibase-manifests)
* Files for [interaction between OpenRefine and KB Wikibases](https://github.com/KBNLresearch/OpenRefine-Wikibase), for reconciling and uploading data to Wikibases of the KB, using Openfine
* [OpenRefine to Wikibase: Data Upload Pipeline](https://en.wikiversity.org/wiki/OpenRefine_to_Wikibase:_Data_Upload_Pipeline)

#### 3) QuickStatements (in bulk)
* "From formatted .txt or .csv to Wikibase"
* [QuickStatements tool](https://meta.wikimedia.org/wiki/QuickStatements) + [help](https://www.wikidata.org/wiki/Help:QuickStatements)
* [QuickStatements interface in KB sandbox WB](https://kbtestwikibase.wikibase.cloud/tools/quickstatements/#/batch) (login required)

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

[About the WBCUG](https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group) - [WBCUG history](https://www.lehir.net/a-short-history-of-the-wikibase-community-user-group/) - [WBCUG members](https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group) - [WBCUG monthly online meetings - The Wikibase Live sessions](https://meta.wikimedia.org/wiki/Category:Wikibase_Community_User_Group/Meetings) - [WBCUG Mailing list](https://lists.wikimedia.org/postorius/lists/wikibaseug.lists.wikimedia.org) ([archives](https://lists.wikimedia.org/hyperkitty/list/wikibaseug@lists.wikimedia.org/)) - [WBCUG Telegram](https://t.me/+WBsf9-C9KPuMZCDT) (or [here](https://t.me/joinchat/HGjGexZ9NE7BwpXzMsoDLA))  
	
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
* Via the meetings, minutes, presentations, mailing lists, socials etc. of the WBCUG, WBSG and WBGNL. See above.
* Wikibase.cloud: [Project updates](https://meta.wikimedia.org/wiki/Wikibase/Wikibase.cloud) - [Mailing list](https://lists.wikimedia.org/postorius/lists/wikibase-cloud.lists.wikimedia.org) ([archives](https://lists.wikimedia.org/hyperkitty/list/wikibase-cloud@lists.wikimedia.org/)) - [Telegram](https://t.me/joinchat/FgqAnxNQYOeAKmyZTIId9g)
* Specifically for libraries:
  - [Wikibase Working Hours](https://www.wikidata.org/wiki/Wikidata:WikiProject_LD4_Wikidata_Affinity_Group/Wikibase_Working_Hours), *community discussion of Wikidata & Wikibase with the goal of understanding how the library can contribute to and leverage these as a platform for publishing, linking, and enriching library linked data.*
  - [IFLA Wikidata Working Group](https://mail.iflalists.org/wws/info/wikidatawg ). *This working group will explore and advocate for the use of and contribution to Wikidata by library and information professionals, the integration of Wikidata and Wikibase with library systems, and alignment of the Wikidata ontology with library metadata formats such as BIBFRAME, RDA, and MARC.*  
* More:
  - [Wikidata Weekly Summary]( https://www.wikidata.org/wiki/Wikidata:Status_updates), also containing WB updates!
  - Wikibase yearly summaries by Envel Le Hir: [2023](https://www.lehir.net/wikibase-yearly-summary-2023), [2022](https://www.lehir.net/wikibase-yearly-summary-2022), [2021](https://www.lehir.net/wikibase-yearly-summary-2021) and [2020](https://www.lehir.net/wikibase-yearly-summary-2020)
  - [Blog by Addshore](https://addshore.com/?s=wikibase), on Wikibase 

<hr>

### Finding help
#### Active help (by humans) 
* Help by community: use all community channels above.
* Tip: Use the Telegram channels if you want help quickly
* Help by Olaf Janssen: [Wikidata user page](https://www.wikidata.org/wiki/User:OlafJanssen) + [Expert page on kb.nl](https://www.kb.nl/over-ons/experts/olaf-janssen)   

#### Passive help (documentation, manuals, HOWTOs, tutorials etc). 
* [Wikibase documentation portal (WMDE)](https://www.mediawiki.org/wiki/Wikibase) + [here](https://www.mediawiki.org/wiki/Wikibase/Using_Wikibase)  
* [Low-level Wikibase technical documentation]( https://doc.wikimedia.org/Wikibase/master/php)
* [Wikibase.cloud documentation portal (WMDE)]( https://www.mediawiki.org/wiki/Wikibase/Wikibase.cloud) + [WB.cloud issue tracker](https://phabricator.wikimedia.org/tag/wikibase.cloud)

#### More help
* [Learning Wikibase](https://learningwikibase.com), a place to learn and share online resources (e.g. articles, videos, workflows, FAQ’s) that make it easier to install, maintain or customize your Wikibase instance. 
* Tip!! [Wikibase resources overview](https://github.com/shigapov/wikibase-knowledge-graphs) by Renat Shigapov 
* [UCLA Library Research Guide on Wikibase and Wikidata](https://guides.library.ucla.edu/semantic-web/wikidata#s-lg-page-section-6895500)  
* [Awesome Wikibase tutorials](https://github.com/shigapov/wikibase-knowledge-graphs#awesome-wikibase-tutorials) collected by Renat Shigapov. 
 


