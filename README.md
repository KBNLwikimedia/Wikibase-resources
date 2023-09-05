<p>
<image src="Afbeelding1.jpg" hspace="10"/>
<image src="KB_Nationale-Bibliotheek_Logo_RGB-Zwart-EN.jpg" width="400" align="top"/>
</p>
		
# Wikibase resources
*A collection of resources, overviews, links and knowlegde related to Wikibase, collected and curated by KB, national library of the Netherlands.*

This overview was originally extracted from the slides of *Introduction Wikibase, the basics*, a lecture for employeees of [KB, national library of the Netherlands](https://www.kb.nl) on 7 September 2023. This slidedeck is availble on [Wikimedia Commons]() and [Zendo]() 

This page is maintained by Olaf Janssen, Wikimedia coordinator of KB [Wikidata user page](https://www.wikidata.org/wiki/User:OlafJanssen) + [Expert page on kb.nl](https://www.kb.nl/over-ons/experts/olaf-janssen) 

Latest update: 5-9-2023

### Contents
  * [Requesting data from a Wikibase](#requesting-data-from-a-Wikibase)
  * [Adding data to a Wikibase](#adding-data-to-a-Wikibase)
  * [Wikibase community](#wikibase-community)
  * [Staying updated](#staying-updated)
  * [Finding help](#finding-help)

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

#### 1) Nieuw item handmatig toevoegen via GUI
O.b.v. KB sandbox WB: https://kbtestwikibase.wikibase.cloud/wiki/Main_Page
https://kbtestwikibase.wikibase.cloud/wiki/Special:NewItem  H.H. ter Balkt https://kbtestwikibase.wikibase.cloud/wiki/Item:Q32   

#### 2) OpenRefine (in bulk)
OpenRefine is a well-known tool for editing, enriching and manipulating data. It is widely used to add data to Wikidata and other Wikibase instances.
OpenRefine-Wikidata workshop, KB, 4-7-2023: https://github.com/KBNLwikimedia/OpenRefine-Introduction-Workshop + https://zenodo.org/record/8207914
Winnaars Halewijn literatuurprijs- Scenario 1 : We willen kijken of deze namen in bepaalde Wikibases voorkomen (reconciliatie). Reconciliatie services van Wikidata, FactGrid, Kunstmuseum en de KB- Scenario 2: We willen (nieuwe, verrijkte, verbeterde) data wegschrijven in (bv.) de KB Wikibase - Koppel OpenRefine aan de KB-Wikibase 
Hoe werken deze scenario's precies? - https://en.wikiversity.org/wiki/OpenRefine_to_Wikibase:_Data_Upload_Pipeline- https://docs.openrefine.org/manual/wikibase/configuration + https://docs.openrefine.org/manual/wikibase/reconciling + https://openrefine.org/docs/manual/wikibase/uploading- https://github.com/KBNLresearch/OpenRefine-Wikibase

#### 3) QuickStatements (in bulk)
: “Van (geformateerde) .txt of .csv naar Wikibase”: https://meta.wikimedia.org/wiki/QuickStatements + https://kbtestwikibase.wikibase.cloud/tools/quickstatements/#/batch + https://www.wikidata.org/wiki/Help:QuickStatements   

#### 4) Geavanceerde data import tools
* [WikibaseImport, a MediaWiki extension: https://github.com/Wikidata/WikibaseImport  
* [WikibaseIntegrator, a Python library: https://github.com/LeMyst/WikibaseIntegrator  + https://pypi.org/project/wikibaseintegrator/0.11.2/  
* [WikidataIntegrator, a Python library: https://github.com/SuLab/WikidataIntegrator  + https://zenodo.org/record/8004921  
* [WikibaseSync, a Python library: https://github.com/the-qa-company/WikibaseSync  +  https://wikibase.the-qa-company.com/wiki/WikibaseSync_-_Tutorial 
* [wikibase-edit, a NodeJS library: https://github.com/maxlath/wikibase-edit  + https://github.com/maxlath/wikibase-edit/blob/master/docs/how_to.md 
* [wikibase-cli, a command-line interface: https://github.com/maxlath/wikibase-cli  
* [VanDerBot, a Python application: https://heardlibrary.github.io/digital-scholarship/lod/wikibase/load/  + https://github.com/HeardLibrary/linked-data/tree/master/vanderbot 
* [Pywikibot, a Python library : https://www.mediawiki.org/wiki/Manual:Pywikibot  + https://github.com/wikimedia/pywikibot + https://doc.wikimedia.org/pywikibot/stable/scripts/wikibase.html  
* [RaiseWikibase, a Python tool: https://github.com/UB-Mannheim/RaiseWikibase 
* [Wikidata-Toolkit, a Java library: https://www.mediawiki.org/wiki/Wikidata_Toolkit + https://github.com/Wikidata/Wikidata-Toolkit  

<hr>

### Wikibase community
Wikibase Community User Group
Its mission is to cultivate Wikibase's development and to encourage like-minded developers and data analysts not only to improve Wikibase's existing tools but also to create new ones. - https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group
WBCUG geschiedenis https://www.lehir.net/a-short-history-of-the-wikibase-community-user-group/ 
WBCUG leden https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group 
WBCUG maandelijkse online bijeenkomsten - The Wikibase Live sessions - https://meta.wikimedia.org/wiki/Category:Wikibase_Community_User_Group/Meetings 
WBCUG Mailing list: https://lists.wikimedia.org/postorius/lists/wikibaseug.lists.wikimedia.org 
WBCUG Telegram: https://t.me/+WBsf9-C9KPuMZCDT + https://t.me/joinchat/HGjGexZ9NE7BwpXzMsoDLA  
	
2) Wikibase Stakeholder Group
Commissions production and maintenance of open source extensions to Wikibase, and documentation for institutions that want to operate and maintain a fully-fledged instance of Wikibase. The group will focus on extensions to Wikibase instead of contributing to Wikibase core. - https://wbstakeholder.group/about
WBSG leden: https://wbstakeholder.group/members
WBSG maandelijkse online bijeenkomsten (notulen): https://notepad.rhizome.org/wikibase-stakeholder-meetings#
WBSG Loomio: https://loomio.rhizome.org/wbsg/
WBSG Mastodon: https://mastodon.social/web/@wbstakeholders // WBSG Twitter: https://twitter.com/wbstakeholders

3) Wikibase Kennisgroep Nederland
Voor iedereen in Nederland die met Wikibase werkt, wil gaan werken of anderszins geïnteresseerd is in deze software. Voornamelijk voor - maar zeker niet beperkt tot - professionals uit Nederlandse erfgoed- en kennisinstellingen, en aanverwante organisaties en bedrijven. - https://www.wikidata.org/wiki/Wikidata:GLAM/Koninklijke_Bibliotheek_Nederland/WikibaseActivities#Dutch_Wikibase_knowledge_group  
WBGNL bijeenkomsten: https://www.wikidata.org/wiki/Wikidata:GLAM/Koninklijke_Bibliotheek_Nederland/WikibaseActivities#Meetings + https://wbstakeholder.group/events/presentations#netherlands-wikibase-knowledge-group
WBGNL mailinglist: https://lists.wmnederland.nl/mailman/listinfo/wikibase-nl
WBGNL Loomio: https://loomio.rhizome.org/wbgn/

4) Losstaande Wikibase workshops, trainingen, meetups, o.a.
Antwerpen, 2018: https://blog.factgrid.de/archives/835
New York, 2018: https://www.wikidata.org/wiki/Wikidata:WikiProject_Wikidata_for_research/Meetups/2018-09-19-21-New-York
Gent, 2019: https://www.wikidata.org/wiki/Wikidata:Events/Belgium/Universiteit_Gent/Wikidata_and_Wikibase_Workshop/2019
Stockholm, 2019:  https://pro.europeana.eu/post/wikidata-wikibase-for-national-libraries-the-inaugural-meeting
Tokyo, 2019: https://twitter.com/andrawaag/status/1178496977723543552
Duitsland, online, 2021: https://nfdi4culture.de/news/wikibase-workshop.html
Online, 2022: https://nfdi4culture.de/events/jcdl-workshop-open-refine-to-wikibase-a-new-data-upload-pipeline
Brussel, 2023: https://joinup.ec.europa.eu/collection/semic-support-centre/event/second-workshop-wikidata-and-wikibase
Wenen, 2023 https://wikibase-lex.sciencesconf.org/  

<hr>

### Staying updated
* Via de meetings, notulen, presentaties, mailinglijsten, socials etc. van de WBCUG, WBSG en WBGNL. – zie overzicht hiervoor.
* Wikibase.cloud: - Project updates Wikibase.cloud: https://meta.wikimedia.org/wiki/Wikibase/Wikibase.cloud- Mailing list Wikibase.cloud:  https://lists.wikimedia.org/postorius/lists/wikibase-cloud.lists.wikimedia.org
* Specifiek voor bibliotheken:- Wikibase Working Hours - Community discussion of Wikidata & Wikibase with the goal of understanding how the library can contribute to and leverage these as a platform for publishing, linking, and enriching library linked data - https://www.wikidata.org/wiki/Wikidata:WikiProject_LD4_Wikidata_Affinity_Group/Wikibase_Working_Hours- IFLA Wikidata Working Group - This working group will explore and advocate for the use of and contribution to Wikidata by library and information professionals, the integration of Wikidata and Wikibase with library systems, and alignment of the Wikidata ontology with library metadata formats such as BIBFRAME, RDA, and MARC - https://mail.iflalists.org/wws/info/wikidatawg  
* More: Wikidata Weekly Summary, bevat ook WB updates! https://www.wikidata.org/wiki/Wikidata:Status_updates  + https://www.wikidata.org/wiki/Topic:Xks1m3byqvkjdhz1  +  https://www.wikidata.org/wiki/Wikidata:Status_updates/2023_06_26- Wikibase yearly summaries (Envel Le Hir): https://www.lehir.net/wikibase-yearly-summary-2022/ (2021, 2020)- Blog Addshore, over Wikibase: https://addshore.com/?s=wikibase 

<hr>

### Finding help
* Active help (by humans) 
  - Help by community: use all community channels above.
  - Tip: Use the Telegram channels if you want help quickly
  - Help by Olaf Janssen: [Wikidata user page](https://www.wikidata.org/wiki/User:OlafJanssen) + [Expert page on kb.nl](https://www.kb.nl/over-ons/experts/olaf-janssen)   

* Passive help (documentation, manuals, HOWTOs, tutorials etc). 
  - Wikibase documentatie portal (WMDE): https://www.mediawiki.org/wiki/Wikibase + https://www.mediawiki.org/wiki/Wikibase/Using_Wikibase  
  - Wikibase technische documentatie (low-level): https://doc.wikimedia.org/Wikibase/master/php
  - Wikibase.cloud documentation portal (WMDE):  https://www.mediawiki.org/wiki/Wikibase/Wikibase.cloud + https://phabricator.wikimedia.org/tag/wikibase.cloud/ (WB.cloud issue tracker)

* More help
  - [Learning Wikibase](https://learningwikibase.com), a place to learn and share online resources (e.g. articles, videos, workflows, FAQ’s) that make it easier to install, maintain or customize your Wikibase instance. - 
  - Tip!! [Wikibase resources overview](https://github.com/shigapov/wikibase-knowledge-graphs) by Renat Shigapov 
  - [UCLA Library Research Guide on Wikibase and Wikidata](https://guides.library.ucla.edu/semantic-web/wikidata#s-lg-page-section-6895500)  
  - [Awesome Wikibase tutorials](https://github.com/shigapov/wikibase-knowledge-graphs#awesome-wikibase-tutorials) collected by Renat Shigapov. 
 


