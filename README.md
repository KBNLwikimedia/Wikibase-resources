<p>
<image src="images/Afbeelding1.jpg" hspace="10"/>
<image src="images/KB_Nationale-Bibliotheek_Logo_RGB-Zwart-EN.jpg" width="400" align="top"/>
</p>
  
# Wikibase resources
*A collection of resources, overviews, links and knowlegde related to Wikibase, collected and curated by KB, national library of the Netherlands.*

<image src="images/Introductie Wikibase de basis KB 7 sept2023 - openingslide.png" width="250" align="right"/>

This page was originally extracted from the slides of the lecture *Introduction Wikibase, the basics*, for employeees of [KB, national library of the Netherlands](https://www.kb.nl) on 7 September 2023. This (rather long) slidedeck is available on [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Introductiecursus_Wikibase_-_Koninklijke_Bibliotheek,_7_september_2023.pdf) and [Zenodo](https://doi.org/10.5281/zenodo.8338811).

This overview is heavily inspired by the *[Wikibase knowledge graphs, A collection of open source tools and resources related to Wikibase knowledge graphs](https://github.com/shigapov/wikibase-knowledge-graphs)* by Renat Shigapov. I've used his centralized overview many times to improve my understanding of the Wikibase universe, and hope to extend it via the overview below, and help others in a similar way.

<hr/>

**Motivation**

I created this page for several reasons:

* As a *textual summary* of my (rather exuberant, visual) [presentation](https://doi.org/10.5281/zenodo.8338811) of September 7th.
* From my own experience (especially if you are new to Wikibase) I know that it can be very time-consuming to discover and understand the different corners of the Wikibase world, and to find your way in this rather confusing forrest/jungle. I hope this *centralized knowledge hub* can help others make that journey a little easier/faster.
* I have only been able to acquire most of my Wikibase knowledge thanks to the openness and generosity of the international Wikibase community and their willingness to make knowledge findable, visible and reusable for free. So I think it is no more than 'good reciprocal decency' to *contribute to the community* this overview of centralized and summarized knowledge.
* As a place to record my *"public personal memory of interesting Wikibase stuff"*.

**Contributing to this page**

This page is maintained by Olaf Janssen, Wikimedia coordinator of KB. See his [Wikidata user page](https://www.wikidata.org/wiki/User:OlafJanssen) and [expert page on kb.nl](https://www.kb.nl/over-ons/experts/olaf-janssen) for contact details.

I plan to improve & expand the overview in the future. If you would like to contribute, please let me know.   

**Reuse and licensing**

This overview can be reused freely and openly, it is available under the [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) license, so attribution is required. Use something like 

*Wikibase resources, Olaf Janssen & KB national library of the Netherlands, https://github.com/KBNLwikimedia/Wikibase-resources* 

<kbd><img src="images/cc-by.png" width="100"/></kbd>

**Latest updates**

Latest update: Version 0.3, 6 December 2023 (added [Wikibase projects for medieval manuscripts](#wikibase-projects-for-medieval-manuscripts))
<hr>

### Contents
- [Recap Wikidata](#recap-wikidata)
  * [Institutional use cases incompatible with Wikidata](#institutional-use-cases-incompatible-with-Wikidata)
- [What is Wikibase?](#what-is-wikibase-)
- [Wikibase courses and tutorials](#wikibase-courses-and-tutorials)
- [Examples of institutions/projects using Wikibase](#examples-of-institutions-projects-using-wikibase)
  * [Wikibase projects in libraries](#wikibase-projects-in-libraries)
  * [Wikibase projects for other GLAMs](#wikibase-projects-for-other-glams)
  * [Wikibase projects for medieval manuscripts](#wikibase-projects-for-medieval-manuscripts)
- [Wikibase components & architecture](#wikibase-components---architecture)
- [Wikibase data model](#wikibase-data-model)
  * [Using alternative vocabularies in Wikibase](#using-alternative-vocabularies-in-wikibase)
- [Wikibase hosting](#wikibase-hosting)
- [Requesting data from a Wikibase](#requesting-data-from-a-wikibase)
  * [Cool Wikibase SPARQL queries](#cool-wikibase-sparql-queries)
- [Adding data to a Wikibase](#adding-data-to-a-wikibase)
- [Wikibase community](#wikibase-community)
- [Staying updated](#staying-updated)
- [Finding help](#finding-help)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

<hr>

### Recap Wikidata
This section ia a summary of the lecture *[Introduction to Wikidata](https://commons.wikimedia.org/wiki/File:Wegwijzer_in_Wikidata,_Introductiecurus_Wikidata_-_Koninklijke_Bibliotheek,_6_juni_2023.pdf)* ([Zenodo](https://zenodo.org/record/8006441)) (in Dutch)

* Wikidata (d.d. 7 Sept 2023) contains structured descriptions of [107 million things](https://www.wikidata.org/wiki/Wikidata:Statistics), since October 2012
* [Wikidata items with geo location](https://commons.wikimedia.org/wiki/File:Wikidata-map-2023-06-26-items-intensity-100.png) (June 2023) - [Older/other maps](https://commons.wikimedia.org/wiki/Wikidata_map) - [Interactive map](https://wmde.github.io/wikidata-map/dist/index.html)
* What are the principles of Wikidata? (see also the [Wikidata introduction](https://www.wikidata.org/wiki/Wikidata:Introduction))
  - Structured descriptions of things, eg. [Eiffel Tower](https://www.wikidata.org/wiki/Q243)
  - Central storage (vs. distributed in data silos)
  - Multilingual (200+ languages) - Description of the Eiffel Tower in [English](https://www.wikidata.org/wiki/Q243?uselang=en), [Dutch](https://www.wikidata.org/wiki/Q243?uselang=nl), [Portuguese](https://www.wikidata.org/wiki/Q243?uselang=pt) and [Japanese](https://www.wikidata.org/wiki/Q243?uselang=ja) etc.
  - Linked data
    - Things, not strings, no flat text strings, but clicklable links
    - Interconcected Wikidata items, eg. [Eiffel Tower](https://www.wikidata.org/wiki/Q243) --> [named after](https://www.wikidata.org/wiki/Property:P138) --> [Gustave Eiffel](https://www.wikidata.org/wiki/Q20882)
    - Wikidata is connected to pm [8.200 external databases](https://rawgit.com/johnsamuelwrites/wdprop/master/datatype.html?datatype=wikibase:ExternalId)
  - Open & free
    - Free, no trackers, no ads, no usage fee.
    - No copyright or database rights, all data is available under the [CC0 license](https://creativecommons.org/publicdomain/zero/1.0/).
    - Everyone can reuse data: query, share, copy , edit, download, sell, etc.
    - Anyone can contribute, edit, add, improve, delete, merge data, etc. --> Community
  - Community
    - International
    - Pm. 24K editors
    - Under the flag of the Wikimedia Foundation. Wikidata is a sister project of Wikipedia, Wikimedia Commons etc.
  - For humans and machines
    - Human readable, human writable --> Data available via [GUIs in HTML](https://www.wikidata.org/wiki/Q1526131)
    - Machine readable, machine writable --> Data available via [APIs in JSON](https://www.wikidata.org/w/api.php?action=wbgetentities&ids=Q1526131) , [XML/RDF](https://www.wikidata.org/w/api.php?action=wbgetentities&ids=Q1526131&props=labels&format=xml), CSV etc.

* Wikidata is a *secondary, general purpose, public* knowledge base for the world.
  - Secondary
    - Non-original data about
    - Notable things ([more info](https://www.wikidata.org/wiki/Wikidata:Notability)) 
    - Verifiable by reliable public sources ([more info](https://www.wikidata.org/wiki/Wikidata:Verifiability))
  - General purpose
    - Wide scope of topics/classes
    - Items contain relatively basic data (limited set of properties), Wikidata is not aimed at superspecialistic/deep data
  - Public
    - Public data
    - Without copyright issues
    - Without privacy issues ([more info](https://www.wikidata.org/wiki/Wikidata:Living_people))

#### Institutional use cases incompatible with Wikidata
* Institutional use cases for which Wikidata is *not* suitable
  - Publish domain-specific / specialist / 'esoteric' LOD
  - Publish very large LOD sets (e.g. catalogues, thesauri)
  - Use of very specific/complex/deep/layered data models
  - Control over who can add/change data
  - Collaboration with selected partners in a closed, controlled environment
  - Recording non-public data
  - Own control over hosting / IT infrastructure

### What is Wikibase?
1. The open-source, free software that powers Wikidata - "Wikibase is essentially a blank copy of Wikidata into which you can put your own structured data" ([source](https://heardlibrary.github.io/digital-scholarship/host/wikidata/bot/)),
2. Allowing you to build & manage your own LOD knowledge base,
3. Without the disadvantages of Wikidata,
   - You can create your own data models, as domain-specific/specialist/esoteric as you want/need.
   - Large data sets are no problem
   - Custom rights management (control over who is allowed to contribute)
   - Wikibase instances can be non-public
   - You can host your own instance
4. With all the benefits of Wikidata
   - Focused on collaboration and connection (including Wikidata community)
   - For people and machines
   - User-friendly GUI for structured data
   - Native multilingualism support
   - Version history and control, rollbacks
   - Clear ontology: Items, Properties, Statements etc.
   - Output in [various data formats](https://www.wikidata.org/wiki/Wikidata:Data_access#Details_2) (including JSON, RDF/XML, N3)
   - Search via [SPARQL](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/A_gentle_introduction_to_the_Wikidata_Query_Service)
   - Well suported and documented [MediaWiki API](https://www.mediawiki.org/wiki/API:Main_page)
   - Support for tools (including [OpenRefine](https://www.openrefine.org))
   - [Documentation for Wikidata](https://www.wikidata.org/wiki/Help:Contents) is in general applicable to Wikibase as well

* *[Wikibase: the advantages of Wikidata, without the disadvantages](https://commons.wikimedia.org/wiki/File:Wikibase,_de_voordelen_van_Wikidata,_zonder_de_nadelen_-_Artikel_van_Olaf_Janssen_in_InformatieProfessional_nr.08,_2019,_pagina_37.jpg)* (article in Dutch by Olaf Janssen) 

* Wikibase website: https://wikiba.se/
* The bigger picture, according to the Wikimedia Foundation: [Wikidata-Wikibase joint vision](https://meta.wikimedia.org/wiki/LinkedOpenData/Strategy2021/Joint_Vision) and the [Wikibase ecosystem](https://meta.wikimedia.org/wiki/LinkedOpenData/Strategy2021/Wikibase)
* [Introduction to Wikibase and Wikibase Cloud](https://www.youtube.com/watch?v=z1Swo5xYKQE) by Georgina Burnett (WMDE), [2022 LD4 conference](https://sites.google.com/berkeley.edu/2022-ld4-conference/home), 12th July 2022 
* [History of Wikibase](https://addshore.com/2022/02/wikibase-a-history/) (until Febr 2022) ([archived version](https://web.archive.org/web/20230714110136/https://addshore.com/2022/02/wikibase-a-history/))

<hr>

### Wikibase courses and tutorials
See also [Awesome Wikibase tutorials](https://github.com/shigapov/wikibase-knowledge-graphs#awesome-wikibase-tutorials) collected by Renat Shigapov.
* [Wikibase and Semantic MediaWiki for data-driven semantics](https://academy.europa.eu/courses/wikibase-and-semantic-mediawiki-for-data-driven-semantics), EU Academy, online <br/>
<sub>In this course, you will learn how community-led tools and platforms like Wikibase, Semantic MediaWiki, and Wikidata can be used to create a data-driven semantic layer in a bottom-up way.</sub>
* [Introduction Wikibase, the basics](https://doi.org/10.5281/zenodo.8338811) by KB, national library of the Netherlands. Also available on [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Introductiecursus_Wikibase_-_Koninklijke_Bibliotheek,_7_september_2023.pdf).

<hr>

### Examples of institutions/projects using Wikibase
* [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) 
* [Rhizome Artbase](https://artbase.rhizome.org/wiki/Main_Page)
  - Rhizome = art organization in NYC
  - Artbase = archive of born-digital art 1983-present.
  - First Wikibase instance outside of Wikimedia projects.
  - [Artworks in the ArtBase with more than one artist](https://artbase.rhizome.org/wiki/Query/example1), visualized as a graph with images. 
* [Enslaved.org](https://enslaved.org)
  - LOD platform containing ±1M records (people, events, places, and sources) related to the transatlantic slave trade
  - *[Stories of the Enslaved told using Wikibase](https://tech-news.wikimedia.de/en/2021/02/18/stories-of-the-enslaved-told-using-wikibase/)*, article by Elisabeth Giesemann, 18 February 2021 
  - [Data dumps from the Wikibase](https://lod.enslaved.org/wiki/Meta:Main_Page) 
* [FactGrid](https://database.factgrid.de/wiki/Main_Page) 
  - Open collaborative international Wikibase knowledge graph for historical research, [312 participants](https://tinyurl.com/2kl7a7gt)
  - [FactGrid projects, by era](https://database.factgrid.de/wiki/FactGrid:Projects), for example [Paris to download](https://database.factgrid.de/wiki/FactGrid:Nineteenth_Century#Paris_to_download), a freely downloadable dataset with geographic coordinates and administrative information from all the houses and streets of Paris in c. 1820. SPARQL: [All the houses and streets of Paris c. 1820](https://tinyurl.com/yf4fvrf7) ([source article](https://blog.factgrid.de/archives/2333) by Bruno Belhoste, 14-11-2021) 
* [The Aviation Safety Network Wikibase](https://aviation-safety.net/wikibase)
  - The [ASN](https://aviation-safety.net/about/) provides up-to-date, complete and reliable authoritative information on airliner accidents and safety issues. 
  - This Wikibase is updated regularly by a large user community and contains descriptions of more than 258,000 accidents involving light aircraft, military aircraft, helicopters, gyroplanes, gliders, hot air balloons and UAVs since 1905.
* [EU Knowlegde Graph](https://linkedopendata.eu/wiki/The_EU_Knowledge_Graph)
  - Contains information about 1.9M projects financed by the EU and 700K beneficiaries of European projects
  - *[Wikibase as an Infrastructure for Knowledge Graphs: the EU Knowledge Graph](https://hal.archives-ouvertes.fr/hal-03353225/document)*, D. Diefenbach, M. De Wilde and S.Alipio, 30 September 2021 -  [WikidataCon 2021 video recording.](https://www.youtube.com/watch?v=PyBWo-ka9JU)
  - [Kohesio website](https://kohesio.ec.europa.eu) is a frontend of the EU Knowledge Graph
  - *[European Commission goes Open Source: New Project Kohesio uses Wikimedia’s Software Wikibase](https://www.wikimedia.de/presse/european-commission-goes-open-source-new-project-kohesio-uses-wikimedias-software-wikibase/)*, 17-03-2022
  - [Explore EU projects in your country/region/neighbourhood](https://kohesio.ec.europa.eu), such as [1.259 EU projects](https://kohesio.ec.europa.eu/nl/?kaart%20regio=Nederland,Zuid-Holland,Q3119) in the Dutch province of South-Holland (dd. Sept 2023) 
* [Kunstmuseum API](https://api.kunstmuseum.nl/wiki/Kunstmuseum_API)
  - Wikibase by [Kunstmuseum Den Haag](https://www.kunstmuseum.nl/en) to import and deliver data for the websites [Delftsaardewerk.nl](https://api.kunstmuseum.nl/wiki/Project/Delftsaardewerk), [Van Gogh Worldwide](https://api.kunstmuseum.nl/wiki/Project/van_Gogh_Worldwide) and [Aziatischekeramiek.nl](https://api.kunstmuseum.nl/wiki/Project/Aziatisch_keramiek) from various museums via a central API.
  - For instance *Object 0400098* in the collection of the Kunstmuseum Den Haag: on [Delftsaardewerk.nl](https://delftsaardewerk.nl/bekijken/voorwerp/gemeentemuseum-den-haag/400098) and [in the Wikibase](https://api.kunstmuseum.nl/wiki/Item:Q2559) 
* Deutsche Nationalbibliothek (DNB) and GND
  - GND = [Gemeinsame Normdatei](https://www.dnb.de/EN/Professionell/Standardisierung/GND/gnd_node.html), Integrated authority file for German speaking countries, 8 M authority records on persons, corporate bodies, subject headings, geographical names, works etc.
  - [Wikibase as a second home for the GND](https://drive.google.com/file/d/1PyUGNeZUx5kmyGJF_cwMPFY4HmT5Kj8_/view) (p. 165) - A Wikibase to collaboratively edit and maintain authority records for the entire GLAM field and digital humanities.
  - *[Could you wikify an authority file? Wikibase has been evaluated for the Integrated Authority File (GND)](https://tech-news.wikimedia.de/en/2020/03/04/wikibase-and-gnd/)* by Barbara Fischer and Jens Ohlig, 4 March 2020
  - See also below, [Wikibase projects in libraries](#wikibase-projects-in-libraries)
* More Wikibase instances
  - [Wikibase World](https://wikibase.world/wiki/Project:Home) - [List of Wikibase instances](https://tinyurl.com/2jkres9t) 
  - [Browse all Wikibase.cloud instances](https://www.wikibase.cloud/discovery)
  - [Awesome Wikibase instances](https://github.com/shigapov/wikibase-knowledge-graphs#awesome-wikibase-instances) by Renat Shigapov

<hr>

### Wikibase projects in libraries
Wikibase is being evaluated by libraries as a tool to help them store and manage their structured data, as well as connect to the world of linked open data. 
* Europe
  - National Library of Germany (DNB), *"GND meets Wikibase", a cooperation*: [Part 1](https://wiki.dnb.de/pages/viewpage.action?pageId=147754828) and [part 2](https://wiki.dnb.de/pages/viewpage.action?pageId=167019461). See also *[A Voice in the Orchestra of Opening the GND](https://drive.google.com/file/d/1PyUGNeZUx5kmyGJF_cwMPFY4HmT5Kj8_/view)* by Barbara Fischer, DNB (p. 145 onwards)
  - German National Library of Science and Technology (TIB): *[Examining Wikidata and Wikibase in the context of research data management applications](https://blogs.tib.eu/wp/tib/2022/03/16/examining-wikidata-and-wikibase-in-the-context-of-research-data-management-applications)* ([video](https://www.youtube.com/watch?v=RPMkuDxHJtI)) and *[Wikidata and Wikibase as complementary research services for cultural heritage data](https://blogs.tib.eu/wp/tib/2022/03/17/wikidata-and-wikibase-as-complementary-research-services-for-cultural-heritage-data/)* (March 2022)
  - TIB/NFDI (Germany): [Linked Open Data Management Services: A Comparison](https://zenodo.org/record/7738424), including Wikibase (15 March 2023)
  - National Library of France (BnF) ([more info](https://commons.wikimedia.org/w/index.php?title=File:Wikibase_for_FNE.pdf)).
  - DBN & BnF: [Wikibase for Cultural Heritage and Academia, Perceived pros and cons of Wikibase as a solution](https://joinup.ec.europa.eu/sites/default/files/custom-page/attachment/2020-11/Parallel-track-4_B-Fischer_J-Thill_A-Angjeli%20final%20ppt.pdf) (slide 7) 
  - National Library of the Czech Republic ([more info](https://blog.wikimedia.cz/2021/09/13/bringing-czech-authority-files-into-21st-century-integration-with-wikidata/)) 
  - National Library of Luxembourg ([more info](https://swib.org/swib21/slides/05-03-gayo.pdf)) 
  - National library of Greece ([more info](https://www.youtube.com/watch?v=TPIS11QK8jI)). See also [Using alternative vocabularies in Wikibase](#using-alternative-vocabularies-in-Wikibase) 
  - National library of the Netherlands (KB)
  - National Library of Wales ([Semantic Name Authority Repository Cymru](https://snarc-llgc.wikibase.cloud/wiki/Main_Page))
* USA
  - The Smithsonian Libraries ([more info](https://blog.library.si.edu/blog/2022/02/17/wikidata-projects/))
  - OCLC, Wikibase pilot, a.k.a. [Project Passage](https://www.oclc.org/content/dam/research/publications/2019/oclcresearch-creating-library-linked-data-with-wikibase-project-passage-a4.pdf) 
  - Academic libraries USA, [Use cases for institutional Wikibase instances](https://github.com/timothy-mendenhall/wikibase-use-cases/blob/master/UseCases-2020.md) 

### Wikibase projects for other GLAMs
* GLAM network Luxembourg ([more info](https://swib.org/swib21/slides/05-03-gayo.pdf)) 
* Europeana EAGLE network - aims to build a multi-lingual online collection of millions of digitised items from European museums, libraries, archives and multi-media collections, which deal with the surviving inscriptions of the Greek-Roman world. The [EAGLE Wikibase](https://wiki.eagle-network.eu/wiki/Main_Page) is designed to give a tool to anyone interested in bridging this gap and contributing translations of inscriptions. 
* Fotomuseum Antwerpen [(more info)](https://fomu.be/kijk-en-lees/het-gevaert-papierproject-ontsluiten-van-een-historische-collectie)

### Wikibase projects for medieval manuscripts

<image src="images/IntroductieWikibase_StudiedagMiddeleeuwseHandschriften_6dec2023 - openingslide.png" width="250" align="right"/>

This section is extracted from the presentation *[Introduction to Wikibase for medieval manuscripts](https://commons.wikimedia.org/wiki/File:Introduction_to_Wikibase_and_medieval_manuscripts_-_Olaf_Janssen_-_06122023.pdf)*  dd 6 December 2023. See the sections about [Digital Scriptorium](https://commons.wikimedia.org/w/index.php?title=File:Introduction_to_Wikibase_and_medieval_manuscripts_-_Olaf_Janssen_-_06122023.pdf&page=48) and [Biblissima](https://commons.wikimedia.org/w/index.php?title=File:Introduction_to_Wikibase_and_medieval_manuscripts_-_Olaf_Janssen_-_06122023.pdf&page=87).  

**Digital Scriptorium**
* [Digital Scriptorium](https://digital-scriptorium.org ) (DS) is a growing consortium of American institutions with collections of global premodern manuscripts dedicated to building an online national union catalog for manuscripts in US collections. 
* The [DS Catalog](https://search.digital-scriptorium.org/) is the first member-supported national union catalog of medieval and early modern manuscripts in US collections built on LOD principles and practices. It connects researchers to pre- and early modern manuscript books in DS member institutions. Built on Wikibase, the DS Catalog aggregates supplied DS member metadata and enriches it by linking to external authorities and resources for enhanced research in a LOD environment.
* Digital Scriptorium catalog 
  - Search for [Book of hours](https://search.digital-scriptorium.org/?f%5Btitle_facet%5D%5B%5D=Book+of+hours ) 
  - First result is [Grolier Club](https://en.wikipedia.org/wiki/Grolier_Club), [MS 07 (DS203)](https://search.digital-scriptorium.org/catalog/DS203)
  - Metadata of DS203:
    - DS ID - Shelfmark - Title - Artist - Place - Date - Language - Physical Description - Former Owner(s) - Note - IIIF Manifest - Holding Institution    
    - [Manuscripts made in France](https://search.digital-scriptorium.org/?f%5Bplace_facet%5D%5B%5D=France)  
    - Wikidata: [Master of the Brotherhood of Ste. Catherine](https://www.wikidata.org/wiki/Q117448635)
    - TGN: [France](http://vocab.getty.edu/tgn/1000070)
    - AAT: [fifteenth century (dates CE)](http://vocab.getty.edu/aat/300404465) 
* The DS catalog metadata originates from the [DS Catalog Wikibase](https://catalog.digital-scriptorium.org)
* [Grolier Club, MS 07 (DS203) in the Wikibase](https://catalog.digital-scriptorium.org/wiki/Item:Q931) (Q931)
  - [Q931](https://catalog.digital-scriptorium.org/wiki/Item:Q931) - Representations [in HTML](https://catalog.digital-scriptorium.org/wiki/Special:EntityData/Q931.html), [JSON](https://catalog.digital-scriptorium.org/wiki/Special:EntityData/Q931.json) or [XML/RDF](https://catalog.digital-scriptorium.org/wiki/Special:EntityData/Q931.rdf)
  - Via the [DS MediaWiki API](https://catalog.digital-scriptorium.org/w/api.php) Q931 can also be requested as [JSON](https://catalog.digital-scriptorium.org/w/api.php?action=wbgetentities&ids=Q931&format=json) or [XML](https://catalog.digital-scriptorium.org/w/api.php?action=wbgetentities&ids=Q931&format=xml)
* Which fields are used in the DS Wikibase? 
  - [Overview of all properties (Ps)](https://catalog.digital-scriptorium.org/wiki/Special:ListProperties). See also the [DS datamodel on Github](https://github.com/DigitalScriptorium/ds-data/blob/main/data-model/ds-model-ids.json)
  - For example: [described manuscript (P3)](https://catalog.digital-scriptorium.org/wiki/Property:P3) - [title as recorded (P10)](https://catalog.digital-scriptorium.org/wiki/Property:P10) - [production date as recorded (P23)](https://catalog.digital-scriptorium.org/wiki/Property:P23) - [production place as recorded (P27)](https://catalog.digital-scriptorium.org/wiki/Property:P27)  
  - Usage of these properties in *[Excerpta ex operibus Sancti Augustini...(DS501)](https://catalog.digital-scriptorium.org/wiki/Item:Q2465)*: [P3](https://catalog.digital-scriptorium.org/wiki/Item:Q2465#P3) - [P10](https://catalog.digital-scriptorium.org/wiki/Item:Q2465#P10) - [P23](https://catalog.digital-scriptorium.org/wiki/Item:Q2465#P23) - [P27](https://catalog.digital-scriptorium.org/wiki/Item:Q2465#P27)
* DS SPARQL queries
  - DS manuscripts: [IDs, Titles, Dates, Places](https://catalog.digital-scriptorium.org/query/#PREFIX%20wd%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2F%3E%0APREFIX%20wdt%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20p%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2F%3E%0APREFIX%20ps%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fstatement%2F%3E%0APREFIX%20pq%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fqualifier%2F%3E%0APREFIX%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0APREFIX%20wikibase%3A%20%3Chttp%3A%2F%2Fwikiba.se%2Fontology%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0A%0ASELECT%20DISTINCT%20%3Frecord%20%3FrecordLabel%20%3FdescribedManuscriptLabel%20%0A%28GROUP_CONCAT%28DISTINCT%20%3FtitleAsRecorded%20%3Bseparator%3D%22%20----%20%22%29%20as%20%3Ftitles%29%20%0A%28GROUP_CONCAT%28DISTINCT%20%3FproductionDateAsRecorded%20%20%3Bseparator%3D%22%20----%20%22%29%20as%20%3FproductionDates%29%20%0A%28GROUP_CONCAT%28DISTINCT%20%3FproductionPlaceAsRecorded%20%3Bseparator%3D%22%20----%20%22%29%20as%20%3FproductionPlaces%29%20%0A%0AWHERE%20%7B%0A%20%20%3Frecord%20p%3AP16%2Fps%3AP16%20wd%3AQ3.%0A%20%20%3Frecord%20p%3AP3%2Fps%3AP3%20%3FdescribedManuscript.%20%0A%20%20%3Frecord%20p%3AP10%2Fps%3AP10%20%3FtitleAsRecorded.%0A%20%20%3Frecord%20p%3AP23%2Fps%3AP23%20%3FproductionDateAsRecorded.%20%0A%20%20%3Frecord%20p%3AP27%2Fps%3AP27%20%3FproductionPlaceAsRecorded%0A%20%20%0ASERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0AGROUP%20BY%20%3Frecord%20%3FrecordLabel%20%3FdescribedManuscriptLabel%20%0AORDER%20BY%20%3FproductionDates%20%3FproductionPlaces), based on [P3](https://catalog.digital-scriptorium.org/wiki/Property:P3), [P10](https://catalog.digital-scriptorium.org/wiki/Property:P10), [P23](https://catalog.digital-scriptorium.org/wiki/Property:P23) and [P27](https://catalog.digital-scriptorium.org/wiki/Property:P27)
  - DS manuscripts: [Names and Roles](https://catalog.digital-scriptorium.org/query/#PREFIX%20wd%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2F%3E%0APREFIX%20wdt%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20p%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2F%3E%0APREFIX%20ps%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fstatement%2F%3E%0APREFIX%20pq%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fqualifier%2F%3E%0APREFIX%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0APREFIX%20wikibase%3A%20%3Chttp%3A%2F%2Fwikiba.se%2Fontology%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0A%0ASELECT%20DISTINCT%20%3Frecord%20%3FrecordLabel%20%3FnameLabel%20%3FroleLabel%0A%0AWHERE%20%7B%0A%20%20%3Frecord%20p%3AP16%2Fps%3AP16%20wd%3AQ3.%0A%20%20%3Frecord%20p%3AP3%2Fps%3AP3%20%3FdescribedManuscript.%20%0A%20%20%3Frecord%20p%3AP14%20%3FassociatedNameAsRecorded.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP17%20%3Fname.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP15%20%3Frole.%0A%20%20%0ASERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0AORDER%20BY%20%3Frecord)
  - DS manuscripts: [Authors and Wikidata linking](https://catalog.digital-scriptorium.org/query/#PREFIX%20wd%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2F%3E%0APREFIX%20wdt%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20p%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2F%3E%0APREFIX%20ps%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fstatement%2F%3E%0APREFIX%20pq%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fqualifier%2F%3E%0APREFIX%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0APREFIX%20wikibase%3A%20%3Chttp%3A%2F%2Fwikiba.se%2Fontology%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0A%0ASELECT%20DISTINCT%20%3Frecord%20%3FrecordLabel%20%3FauthorLabel%20%3FauthorWikidataQid%20%3FauthorWikidataURI%0A%0AWHERE%20%7B%0A%20%20%3Frecord%20p%3AP16%2Fps%3AP16%20wd%3AQ3.%0A%20%20%3Frecord%20p%3AP3%2Fps%3AP3%20%3FdescribedManuscript.%20%0A%20%20%3Frecord%20p%3AP14%20%3FassociatedNameAsRecorded.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP17%20%3Fauthor.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP15%20%3Frole.%0A%20%20FILTER%20%28%3Frole%20%3D%20wd%3AQ18%29%20%23%20filter%20for%20role%3Dauthor%0A%20%20%3Fauthor%20wdt%3AP42%20%3FauthorWikidataQid%0A%20%20BIND%28URI%28CONCAT%28%22http%3A%2F%2Fwww.wikidata.org%2Fentity%2F%22%2C%20%3FauthorWikidataQid%29%29%20as%20%3FauthorWikidataURI%29%0A%20%20%0ASERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0AORDER%20BY%20%3Frecord) - Example author: [Charles VIII of France](https://www.wikidata.org/wiki/Q134452) 
  - [Portraits of DS authors from Wikidata](https://catalog.digital-scriptorium.org/query/#PREFIX%20wd%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2F%3E%0APREFIX%20wdt%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20p%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2F%3E%0APREFIX%20ps%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fstatement%2F%3E%0APREFIX%20pq%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fqualifier%2F%3E%0A%0APREFIX%20wdt_wd%3A%20%3Chttp%3A%2F%2Fwww.wikidata.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20wd_wd%3A%20%3Chttp%3A%2F%2Fwww.wikidata.org%2Fentity%2F%3E%0A%0APREFIX%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0APREFIX%20wikibase%3A%20%3Chttp%3A%2F%2Fwikiba.se%2Fontology%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0A%0A%23defaultView%3AImageGrid%0ASELECT%20DISTINCT%20%3Frecord%20%3FrecordLabel%20%3FauthorLabel%20%3FauthorWikidataURI%20%3FauthorWikidataPortrait%0AWHERE%20%7B%0A%20%20%3Frecord%20p%3AP16%2Fps%3AP16%20wd%3AQ3.%0A%20%20%3Frecord%20p%3AP3%2Fps%3AP3%20%3FdescribedManuscript.%20%0A%20%20%3Frecord%20p%3AP14%20%3FassociatedNameAsRecorded.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP17%20%3Fauthor.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP15%20%3Frole.%0A%20%20FILTER%20%28%3Frole%20%3D%20wd%3AQ18%29%20%23%20filter%20for%20role%3Dauthor%0A%20%20%3Fauthor%20wdt%3AP42%20%3FauthorWikidataQid%0A%20%20BIND%28URI%28CONCAT%28%22http%3A%2F%2Fwww.wikidata.org%2Fentity%2F%22%2C%20%3FauthorWikidataQid%29%29%20as%20%3FauthorWikidataURI%29%0A%20%20%0A%20%20SERVICE%20%3Chttps%3A%2F%2Fquery.wikidata.org%2Fsparql%3E%20%7B%0A%20%20%20%20%20%20%3FauthorWikidataURI%20wdt_wd%3AP31%20%3FIsA.%0A%20%20%20%20%20%20FILTER%20%28%3FIsA%20%3D%20wd_wd%3AQ5%29%20%23%20filter%20in%20Wikidata%20for%20only%20humans%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%0A%20%20%20%20%20%20%3FauthorWikidataURI%20wdt_wd%3AP18%20%3FauthorWikidataPortrait%0A%20%20%7D%20%20%20%0ASERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0AORDER%20BY%20%3Frecord)
  - More [DS SPARQL queries on Github](https://github.com/DigitalScriptorium/ds-testing/tree/main/sparql), such as [this example](https://github.com/DigitalScriptorium/ds-testing/blob/main/sparql/beta/find-manuscripts/by-language/all), which can be [run in the SPARQL interface](https://catalog.digital-scriptorium.org/query/#PREFIX%20wd%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2F%3E%0APREFIX%20wds%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2Fstatement%2F%3E%0APREFIX%20wdv%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fvalue%2F%3E%0APREFIX%20wdt%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20p%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2F%3E%0APREFIX%20ps%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fstatement%2F%3E%0APREFIX%20pq%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fqualifier%2F%3E%0A%0APREFIX%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0APREFIX%20wikibase%3A%20%3Chttp%3A%2F%2Fwikiba.se%2Fontology%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0A%0A%23%20find%20manuscript%20records%20and%20associated%20languages%0ASELECT%20%3Frecord%20%3FrecordLabel%20%3FlanguageString%20%3FlanguageLabel%20%3FQID%0AWHERE%20%7B%0A%23%20bind%20query%20variables%0A%20%20BIND%28p%3AP21%20AS%20%3FlanguageAsRecordedStatement%29.%0A%20%20BIND%28ps%3AP21%20AS%20%3FlanguageAsRecorded%29.%0A%20%20BIND%28pq%3AP22%20AS%20%3FlanguageInAuthority%29.%0A%20%20BIND%28wdt%3AP42%20AS%20%3FhasQID%29.%0A%23%20statement%3A%20manuscript%20record%20has%20statement%20for%20language%0A%20%20%3Frecord%20%3FlanguageAsRecordedStatement%20%3FlanguageStatement%20.%0A%23%20statement%3A%20language%20statement%20has%20language%20object%20recorded%20as%20string%20value%0A%20%20%3FlanguageStatement%20%3FlanguageAsRecorded%20%3FlanguageString%20.%0A%23%20statement%3A%20language%20statement%20has%20qualifier%20for%20possible%20structured%2Fauthority%20value%2C%20which%20may%20have%20QID%0A%20%20OPTIONAL%20%7B%7B%20%3FlanguageStatement%20%3FlanguageInAuthority%20%3Flanguage%20.%7D%20%7B%20%3Flanguage%20%3FhasQID%20%3FQID%20.%7D%7D%0A%20%20%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22.%20%7D%0A%20%20%7D%0AORDER%20by%20%3FrecordLabel%20%3FlanguageLabel).  
* DS overview article: [Wikibase Model for Premodern Manuscript Metadata Harmonization, Linked Data Integration, and Discovery](https://dl.acm.org/doi/full/10.1145/3594723) - Mikko Koho, L. P. Coladangelo, Lynn Ransom, and Doug Emery. 2023. J. Comput. Cult. Herit. 16, 3, Article 56 (September 2023), 25 pages. https://doi.org/10.1145/3594723  
* [DS Github](https://github.com/DigitalScriptorium) 

**Biblissima**
* [Biblissima+](https://projet.biblissima.fr/en) is a French multi-site digital infrastructure for research and service dedicated to the history of the transmission of ancient texts, from Antiquity to the Renaissance, in the West and in the East.
* Biblissima services: [Project site](https://projet.biblissima.fr/en) - [Portal](https://portail.biblissima.fr) - [IIIF](https://iiif.biblissima.fr) - [Toolkit](https://outils.biblissima.fr) - [Documentation](https://doc.biblissima.fr/) - [Demos](https://demos.biblissima.fr/) - **[Wikibase](https://data.biblissima.fr/w/Accueil/en)** 
* [Biblissima Wikibase](https://data.biblissima.fr/w/Accueil/en): Biblissima's authority files
  * [Available entitiy types](https://data.biblissima.fr/w/Project:Types_d%27entit%C3%A9s) in this Wikibase. Eg.
    - [Persons/humans](https://data.biblissima.fr/w/Sp%C3%A9cial:Pages_li%C3%A9es/Item:Q168), such as [Aaron Wolf Herlingen (1700?-1768?)](https://data.biblissima.fr/w/Item:Q200) 
    - [Manuscripts](https://data.biblissima.fr/w/Sp%C3%A9cial:Pages_li%C3%A9es/Item:Q32810 ), such as [Paris. Bibliothèque de l'Arsenal, 1015](https://data.biblissima.fr/w/Item:Q32957)
  * [All Biblissima Wikibase properties](https://data.biblissima.fr/w/Sp%C3%A9cial:ListProperties) (295 Ps)
  * Links to other databases: [External IDs](https://data.biblissima.fr/w/Sp%C3%A9cial:ListProperties/?datatype=external-id) (213 Ps)
  * [Currently no Biblissima SPARQL query service available!](https://data.biblissima.fr/w/Project:API#Point_d'acc%C3%A8s_SPARQL) 


<hr>

### Wikibase components & architecture 
Diefenbach et al. (2021), *[Wikibase as an Infrastructure for Knowledge Graphs: the EU Knowledge Graph](https://hal.science/hal-03353225/document)*, see "3.1 Wikibase infrastructure"  
* [Wikibase architecture documentation](https://wmde.github.io/wikidata-wikibase-architecture ) 

<hr>

### Wikibase data model
* [Simplified Wikibase data model](https://www.mediawiki.org/wiki/Wikibase/DataModel/Primer) 
* EU Knowledge Graph: “Amsterdam is the capital of the Netherlands" --> Triple:
  - Item = [The Netherlands (Q19)](https://linkedopendata.eu/wiki/Item:Q19)
  - Property = [Captital city (P27)](https://linkedopendata.eu/wiki/Property:P27)
  - Value: [Amsterdam (Q43)](https://linkedopendata.eu/wiki/Item:Q43)
* [Version history and rollback](https://linkedopendata.eu/w/index.php?title=Item:Q43&action=history) (for Q43)
* [Wikibase conceptual data model](https://www.mediawiki.org/wiki/Wikibase/DataModel) 

#### Using alternative vocabularies in Wikibase 
* As explained [above](#wikibase-data-model) Wikibase has its own unique data model, which has its limitations. To what extent can other vocabularies (such as [RDA](https://en.wikipedia.org/wiki/Resource_Description_and_Access) and [Schema.org](https://en.wikipedia.org/wiki/Schema.org)) be included into a Wikibase?
* Literature explaining the limitations of the Wikibase model:
  - *[Analysing and promoting ontology interoperability in Wikibase](https://wikidataworkshop.github.io/2022/papers/Wikidata_Workshop_2022_paper_9774.pdf)*, D.Dobriy and A. Polleres (2022)
  - *[Wikibase as an Infrastructure for Knowledge Graphs: the EU Knowledge Graph](https://hal.science/hal-03353225/document)*, Diefenbach et al. (2021), see "5. Comparing classical approach vs Wikibase"  
  - *[Wikibase, or The search for the unicorn](https://doi.org/10.36253/jlis.it-484)*, Bergamin, G. (2022), JLIS.It, 13(3), 49–62. 
* Analysis of the problem by Marieke Moolenaar (KB, August 2023)<br/>
<sub>*Wikibase uses a derivative of Blazegraph as its linked data storage. Let's call this the Wikibase-Blazegraph-DB. Blazegraph is a so-called graph DB or triple store, so you should be able to store RDF triples in it, thus also RDA/RDF triples and Schema.org triples. Currently, default Wikibase instances are set up in such a way that only Wikibase Q-P-Q triples can be included in the Wikibase-Blazegraph-DB via an update process from the MediaWiki-MySQL database. Schema.org or RDA/RDF triples can never enter the Wikibase-Blazegraph-DB via that update process. So if you want to get triples with other vocabulary into the KB-Wikibase-Blazegraph-DB, you will have to put them in there via another way than via the Wikibase-MediaWiki-GUI and the MediaWiki-MySQL database upate process.*</sub>
* Workaround by National library of Greece (NLG) - [Implementing RDA in Wikibase](http://www.rda-rsc.org/sites/all/files/NLG_Wikibase.pdf), C. Bratsas and L. Ioannidis of Open Knowledge Greece
* Summary of the NLG approach written by Marieke Moolenaar (KB, August 2023):<br/>
<sub>*The Greek Wikibase is only used as a graphical interface (front-end) for entering thesaurus data by library staff.
They do *not* use their Wikibase to publish linked data, but only for data entry purposes. The reason they do not use Wikibase for publishing linked data is that in Wikibase you can only use the proprietary Wikibase metadata model, thus external vocabularies (such as RDA/RDF) cannot be used in Wikibase. To be able to enter new thesaurus triples via Wikibase screens/GUI, the NLG has made a translation/mapping from RDA/RDF to Wikibase entities (Ps and Qs). They periodically copy all created thesaurus triples from the Wikibase graph to another triple store ([Triply](https://triply.cc/)). To do this, they translate their Wikibase triples back to RDA/RDF triples. In Triply they store and publish the real RDA/RDF vocabulary triples, which are not (or cannot be) present in Wikibase.*</sub>
* [How to load up schema.org data dumps into Blazegraph](https://github.com/schemaorg/schemaorg/wiki/BlazeGraphSPARQLHowto) by Dan Brickley, August 2016  

<hr>

### Wikibase hosting
* [Which Wikibase should I choose?](https://www.mediawiki.org/wiki/Wikibase/Which) 
* [Wikibase Suite](https://www.mediawiki.org/wiki/Wikibase/Suite) and [Wikibase Docker](https://www.mediawiki.org/wiki/Wikibase/Docker) - software that you install and run on your own hardware (typically via Docker). Good for users who want to try out Wikibase on their own hardware and who want to customize their installation. Good for institutions with large datasets.
* [Wikibase.cloud](https://www.wikibase.cloud) - free “Wikibase as a service” platform  to create Wikibases quickly and easily managed and maintained by Wikimedia Deutschland.
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
* [Digital Scriptorium](https://catalog.digital-scriptorium.org/wiki/Main_Page):
  * [Manuscripts: Titles, dates, places](https://tinyurl.com/yuxkeugj)
  * [Manuscripts: Names + roles](https://tinyurl.com/yos7otvz)
  * [Manuscripts: Authors + Wikidata links](https://catalog.digital-scriptorium.org/query/#PREFIX%20wd%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2F%3E%0APREFIX%20wdt%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20p%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2F%3E%0APREFIX%20ps%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fstatement%2F%3E%0APREFIX%20pq%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fqualifier%2F%3E%0APREFIX%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0APREFIX%20wikibase%3A%20%3Chttp%3A%2F%2Fwikiba.se%2Fontology%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0A%0ASELECT%20DISTINCT%20%3Frecord%20%3FrecordLabel%20%3FauthorLabel%20%3FauthorWikidataQid%20%3FauthorWikidataURI%0A%0AWHERE%20%7B%0A%20%20%3Frecord%20p%3AP16%2Fps%3AP16%20wd%3AQ3.%0A%20%20%3Frecord%20p%3AP3%2Fps%3AP3%20%3FdescribedManuscript.%20%0A%20%20%3Frecord%20p%3AP14%20%3FassociatedNameAsRecorded.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP17%20%3Fauthor.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP15%20%3Frole.%0A%20%20FILTER%20%28%3Frole%20%3D%20wd%3AQ18%29%20%23%20filter%20for%20role%3Dauthor%0A%20%20%3Fauthor%20wdt%3AP42%20%3FauthorWikidataQid%0A%20%20BIND%28URI%28CONCAT%28%22http%3A%2F%2Fwww.wikidata.org%2Fentity%2F%22%2C%20%3FauthorWikidataQid%29%29%20as%20%3FauthorWikidataURI%29%0A%20%20%0ASERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0AORDER%20BY%20%3Frecord) 
  * [Authors: Portraits from Wikidata](https://catalog.digital-scriptorium.org/query/#PREFIX%20wd%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fentity%2F%3E%0APREFIX%20wdt%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20p%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2F%3E%0APREFIX%20ps%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fstatement%2F%3E%0APREFIX%20pq%3A%20%3Chttps%3A%2F%2Fcatalog.digital-scriptorium.org%2Fprop%2Fqualifier%2F%3E%0A%0APREFIX%20wdt_wd%3A%20%3Chttp%3A%2F%2Fwww.wikidata.org%2Fprop%2Fdirect%2F%3E%0APREFIX%20wd_wd%3A%20%3Chttp%3A%2F%2Fwww.wikidata.org%2Fentity%2F%3E%0A%0APREFIX%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0APREFIX%20wikibase%3A%20%3Chttp%3A%2F%2Fwikiba.se%2Fontology%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0A%0A%23defaultView%3AImageGrid%0ASELECT%20DISTINCT%20%3Frecord%20%3FrecordLabel%20%3FauthorLabel%20%3FauthorWikidataURI%20%3FauthorWikidataPortrait%0AWHERE%20%7B%0A%20%20%3Frecord%20p%3AP16%2Fps%3AP16%20wd%3AQ3.%0A%20%20%3Frecord%20p%3AP3%2Fps%3AP3%20%3FdescribedManuscript.%20%0A%20%20%3Frecord%20p%3AP14%20%3FassociatedNameAsRecorded.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP17%20%3Fauthor.%0A%20%20%3FassociatedNameAsRecorded%20pq%3AP15%20%3Frole.%0A%20%20FILTER%20%28%3Frole%20%3D%20wd%3AQ18%29%20%23%20filter%20for%20role%3Dauthor%0A%20%20%3Fauthor%20wdt%3AP42%20%3FauthorWikidataQid%0A%20%20BIND%28URI%28CONCAT%28%22http%3A%2F%2Fwww.wikidata.org%2Fentity%2F%22%2C%20%3FauthorWikidataQid%29%29%20as%20%3FauthorWikidataURI%29%0A%20%20%0A%20%20SERVICE%20%3Chttps%3A%2F%2Fquery.wikidata.org%2Fsparql%3E%20%7B%0A%20%20%20%20%20%20%3FauthorWikidataURI%20wdt_wd%3AP31%20%3FIsA.%0A%20%20%20%20%20%20FILTER%20%28%3FIsA%20%3D%20wd_wd%3AQ5%29%20%23%20filter%20in%20Wikidata%20for%20only%20humans%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%0A%20%20%20%20%20%20%3FauthorWikidataURI%20wdt_wd%3AP18%20%3FauthorWikidataPortrait%0A%20%20%7D%20%20%20%0ASERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0AORDER%20BY%20%3Frecord)
   * More DS SPARQL queries [via Github](https://github.com/DigitalScriptorium/ds-testing/tree/main/sparql)      
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

[About the WBSG](https://wbstakeholder.group/about) - [WBSG members](https://wbstakeholder.group/members) - [WBSG meeting calender](https://notepad.rhizome.org/wbsg-services) - [WBSG monthly online meeting minutes](https://notepad.rhizome.org/wikibase-stakeholder-meetings#)  - [WBSG Loomio](https://loomio.rhizome.org/wbsg/) - [WBSG Mastodon](https://mastodon.social/web/@wbstakeholders) - [WBSG Twitter](https://twitter.com/wbstakeholders)

#### 3) Wikibase Knowlegde Group Netherlands (WBGNL)
*The aim of this group is to bundle and exchange knowledge & experiences about the use of Wikibase, to learn from each other, and to keep each other informed about the (international) developments and opportunities surrounding Wikibase. Membership is open to everyone in the Netherlands who already works with Wikibase, wants to work with, or is otherwise interested in this software. Mainly for - but certainly not limited to - professionals from Dutch heritage and knowledge institutions, and related organizations and companies.*  

[About the WBGNL](https://www.wikidata.org/wiki/Wikidata:GLAM/Koninklijke_Bibliotheek_Nederland/WikibaseActivities#Dutch_Wikibase_knowledge_group) - [WBGNL meetings](https://wbstakeholder.group/events/presentations#netherlands-wikibase-knowledge-group) (also available [here](https://www.wikidata.org/wiki/Wikidata:GLAM/Koninklijke_Bibliotheek_Nederland/WikibaseActivities#Meetings)) - [WBGNL mailing list](https://lists.wmnederland.nl/mailman/listinfo/wikibase-nl) - [WBGNL Loomio](https://loomio.rhizome.org/wbgn/)

#### 4) Wikibase community workshops, trainings, meetups etc. (archive)
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

<hr/>

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

#### Passive help (documentation, manuals, HOWTOs, tutorials etc.)
* [Wikibase documentation portal (WMDE)](https://www.mediawiki.org/wiki/Wikibase) + [here](https://www.mediawiki.org/wiki/Wikibase/Using_Wikibase)  
* [Low-level Wikibase technical documentation]( https://doc.wikimedia.org/Wikibase/master/php)
* [Wikibase.cloud documentation portal (WMDE)]( https://www.mediawiki.org/wiki/Wikibase/Wikibase.cloud) + [WB.cloud issue tracker](https://phabricator.wikimedia.org/tag/wikibase.cloud)

#### More help
* [Learning Wikibase](https://learningwikibase.com), a place to learn and share online resources (e.g. articles, videos, workflows, FAQ’s) that make it easier to install, maintain or customize your Wikibase instance. 
* Tip!! [Wikibase resources overview](https://github.com/shigapov/wikibase-knowledge-graphs) by Renat Shigapov 
* [UCLA Library Research Guide on Wikibase and Wikidata](https://guides.library.ucla.edu/semantic-web/wikidata#s-lg-page-section-6895500)  

