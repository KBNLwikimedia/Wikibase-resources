<p>
<image src="Afbeelding1.jpg" hspace="10"/>
<image src="KB_Nationale-Bibliotheek_Logo_RGB-Zwart-EN.jpg" width="400" align="top"/>
</p>
  
# Wikibase resources
*A collection of resources, overviews, links and knowlegde related to Wikibase, collected and curated by KB, national library of the Netherlands.*

**Work in progress!!**

This overview was originally extracted from the slides of the lecture *Introduction Wikibase, the basics*, for employeees of [KB, national library of the Netherlands](https://www.kb.nl) on 7 September 2023. This slidedeck is available on [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Introductiecursus_Wikibase_-_Koninklijke_Bibliotheek,_7_september_2023.pdf) and [Zenodo](https://doi.org/10.5281/zenodo.8338811).

This overview is heavily inspired by the *[Wikibase knowledge graphs, A collection of open source tools and resources related to Wikibase knowledge graphs](https://github.com/shigapov/wikibase-knowledge-graphs)* by Renat Shigapov. I've used this overview many times to improve my understanding of the Wikibase universe, and hope to extend it via the overview below, and help others in a similar way.

This page is maintained by Olaf Janssen, Wikimedia coordinator of KB. See his [Wikidata user page](https://www.wikidata.org/wiki/User:OlafJanssen) and [expert page on kb.nl](https://www.kb.nl/over-ons/experts/olaf-janssen) for contact details.

Latest update: 13 September 2023
<hr>

### Contents
- [Wikibase resources](#wikibase-resources)
  + [Wikibase hosting](#wikibase-hosting)
  + [Requesting data from a Wikibase](#requesting-data-from-a-wikibase)
  + [Cool Wikibase SPARQL queries](#cool-wikibase-sparql-queries)
  + [Adding data to a Wikibase](#adding-data-to-a-wikibase)
  + [Wikibase community](#wikibase-community)
  + [Staying updated](#staying-updated)
  + [Finding help](#finding-help)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

<hr>

[History of Wikibase](https://addshore.com/2022/02/wikibase-a-history/) (until Febr 2022) ([archived version](https://web.archive.org/web/20230714110136/https://addshore.com/2022/02/wikibase-a-history/))

<hr>

### Recap Wikidata
This section ia a summary of the lecture *[Introduction to Wikidata](https://commons.wikimedia.org/wiki/File:Wegwijzer_in_Wikidata,_Introductiecurus_Wikidata_-_Koninklijke_Bibliotheek,_6_juni_2023.pdf)* ([Zenodo](https://zenodo.org/record/8006441)) (in Dutch)

* Wikidata (d.d. 7 Sept 2023) contains structured descriptions of [107 million things](https://www.wikidata.org/wiki/Wikidata:Statistics), since October 2012
* [Wikidata items with geo location](https://commons.wikimedia.org/wiki/File:Wikidata_Map_May_2019_Huge.png) (as of May 2019)
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

#### Institutional requirements
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
  - [Wikibase World](https://wikibase.world/wiki/Project:Home) - [List of WB instances](https://tinyurl.com/2jkres9t)
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
* USA
  - The Smithsonian Libraries ([more info](https://blog.library.si.edu/blog/2022/02/17/wikidata-projects/))
  - OCLC, Wikibase pilot, a.k.a. [Project Passage](https://www.oclc.org/content/dam/research/publications/2019/oclcresearch-creating-library-linked-data-with-wikibase-project-passage-a4.pdf) 
  - Academic libraries USA, [Use cases for institutional Wikibase instances](https://github.com/timothy-mendenhall/wikibase-use-cases/blob/master/UseCases-2020.md) 
<hr>

### WB components & architecture 
* Diefenbach et al. (2021), *[Wikibase as an Infrastructure for Knowledge Graphs: the EU Knowledge Graph](https://hal.science/hal-03353225/document)*, see "3.1 Wikibase infrastructure"  
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
* Solution by National library of Greece (NLG) - [Implementing RDA in Wikibas](http://www.rda-rsc.org/sites/all/files/NLG_Wikibase.pdf), C. Bratsas and L. Ioannidis of Open Knowledge Greece
* Summary of the NLG approach written by Marieke Moolenaar (KB, internal email, 21-8-2023):<br/>
<sub>*The Greek Wikibase is only used as a graphical interface (front-end) for entering thesaurus data by library staff.
They do *not* use their Wikibase to publish linked data, but only for data entry purposes. The reason they do not use Wikibase for publishing linked data is that in Wikibase you can only use the proprietary Wikibase metadata model, thus external vocabularies (such as RDA/RDF) cannot be used in Wikibase. To be able to enter new thesaurus triples via Wikibase screens/GUI, the NLG has made a translation/mapping from RDA/RDF to Wikibase entities (Ps and Qs). They periodically copy all created thesaurus triples from the Wikibase graph to another triple store ([Triply](https://triply.cc/)). To do this, they translate their Wikibase triples back to RDA/RDF triples. In Triply they store and publish the real RDA/RDF vocabulary triples, which are not (or cannot be) present in Wikibase.*</sub>
* [How to load up schema.org data dumps into Blazegraph](https://github.com/schemaorg/schemaorg/wiki/BlazeGraphSPARQLHowto) by Dan Brickley, August 2016  

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

#### Passive help (documentation, manuals, HOWTOs, tutorials etc.)
* [Wikibase documentation portal (WMDE)](https://www.mediawiki.org/wiki/Wikibase) + [here](https://www.mediawiki.org/wiki/Wikibase/Using_Wikibase)  
* [Low-level Wikibase technical documentation]( https://doc.wikimedia.org/Wikibase/master/php)
* [Wikibase.cloud documentation portal (WMDE)]( https://www.mediawiki.org/wiki/Wikibase/Wikibase.cloud) + [WB.cloud issue tracker](https://phabricator.wikimedia.org/tag/wikibase.cloud)

#### More help
* [Learning Wikibase](https://learningwikibase.com), a place to learn and share online resources (e.g. articles, videos, workflows, FAQ’s) that make it easier to install, maintain or customize your Wikibase instance. 
* Tip!! [Wikibase resources overview](https://github.com/shigapov/wikibase-knowledge-graphs) by Renat Shigapov 
* [UCLA Library Research Guide on Wikibase and Wikidata](https://guides.library.ucla.edu/semantic-web/wikidata#s-lg-page-section-6895500)  
* [Awesome Wikibase tutorials](https://github.com/shigapov/wikibase-knowledge-graphs#awesome-wikibase-tutorials) collected by Renat Shigapov. 
 


