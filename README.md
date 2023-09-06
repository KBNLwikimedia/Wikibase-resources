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

Latest update: 7 September 2023
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
Dit blok is een samenvatting van de presentatie Wegwijzer in Wikidata, Olaf Janssen, KB, 6 juni 2023
https://commons.wikimedia.org/wiki/File:Wegwijzer_in_Wikidata,_Introductiecurus_Wikidata_-_Koninklijke_Bibliotheek,_6_juni_2023.pdf 
Zenodo: https://zenodo.org/record/8006441

Wikidata bevat gestructureerde beschrijvingen van 106M dingen sinds okt 2012, volgens https://www.wikidata.org/wiki/Wikidata:Statistics, dd 3-5-2023
o.a: Wetenschappelijke artikelen - Mensen - Dieren en planten - Gebeurtenissen - Landen, provincies, gemeentes, steden, dorpen - Straten, wegen, pleinen - Gebouwen - Voertuigen - Bedrijven en instellingen - Kunstwerken (film, muziek, schilderijen etc.) - Chemische stoffen - Astromische objecten - Genen - e.v.a.
Wikidata-items met geolocatie, mei 2019 - https://commons.wikimedia.org/wiki/File:Wikidata_Map_May_2019_Huge.png, Addshore, CC0, via Wikimedia Commons

Wat zijn de uitgangspunten van Wikidata? 
1. Gestructureerde beschrijvingen van dingen
2. Centrale opslag (vs gedistribueerd – data silo’s)
3. Meertalig (200+ talen) - Beschrijving van de Eiffeltoren - https://www.wikidata.org/wiki/Q243 (Nederlandstalige, Engelstalige, Portugese en Japanse interface)
4. Linked data - Things, not strings - Geen platte tekst, maar klikbare links - Onderling verbonden: https://www.wikidata.org/wiki/Q243 (Eiffeltoren) en https://www.wikidata.org/wiki/Q20882 (Gustave Eiffel) - Verbonden met andere databases
5. Open & vrij - Gratis, geen trackers, geen ads - Geen auteurs- of databankrechten (CC0-licentie - https://creativecommons.org/publicdomain/zero/1.0/) - Iedereen mag data hergebruiken: bevragen, delen, kopiëren, bewerken, downloaden, verkopen etc. - Iedereen mag data bijdragen/bewerken toevoegen, verbeteren, verwijderen, samenvoegen etc. --> community
6. Community - Internationaal - 24K bewerkers - Onder de vlag van de Wikimedia Foundation  zusterproject van Wikipedia, Commons etc. 
7. Voor mensen en machines - Mensleesbaar, mensschrijfbaar --> Data beschikbaar via GUIs in HTML, https://www.wikidata.org/wiki/Q1526131 (Koninklijke bibliotheek) - Machineleesbaar, machineschrijfbaar --> Data beschikbaar via APIs in JSON, XML/RDF, CSV etc.,  https://www.wikidata.org/w/api.php?action=wbgetentities&ids=Q1526131   https://www.wikidata.org/w/api.php?action=wbgetentities&ids=Q1526131&props=labels&format=xml 

<hr>
Wat voor soort data bevat Wikidata? https://kennisplatform.wikimedia.nl/artikelen/data-delen/wat-zijn-de-criteria-voor-data-op-wikidata/ 
Wikidata is een secundaire, algemene, openbare kennisbank voor de wereld.

* Secundair
  - Niet-originele gegevens over
  - Notenswaardige dingen (meer info) 
  - Verifieerbaar d.m.v. betrouwbare openbare bronnen (meer info)
* Algemeen
  - Breed scala aan onderwerpen/klassen
  - Relatief basale data, niet superspecialistisch
* Openbaar
  - Openbare gegevens
  - Geen auteursrechten
  - Geen privacygevoeligheden (meer info)

<hr>
Wensen van erfgoedinstellingen waarvoor Wikidata niet geschikt is
* Publiceren domein-specifieke / specialistische / ‘esoterische’ LOD
* Publiceren hele grote LOD-sets (bv. catalogi, thesauri)
* Gebruik hele specifieke/complexe/gelaagde/diepe datamodellen
* Eigen controle over wie data mag toevoegen / muteren
* Samenwerking met geselecteerde partners in besloten, gecontroleerde omgeving
* Vastleggen niet-openbare data
* Eigen controle over hosting / IT-infra

Wikibase als oplossing!? https://commons.wikimedia.org/wiki/File:Wikibase,_de_voordelen_van_Wikidata,_zonder_de_nadelen_-_Artikel_van_Olaf_Janssen_in_InformatieProfessional_nr.08,_2019,_pagina_37.jpg, Olaf Janssen, CC BY-SA 4.0

### Wat is Wikibase?
* De open-source, gratis software waar Wikidata op draait - Wikibase is essentially a blank copy of Wikidata into which you can put your own structured data. Bron
* Je kunt er je eigen LOD-kennisbank mee bouwen & beheren
* Zonder de nadelen van Wikidata 
  - Eigen datamodellen, domein-specifiek / specialistisch / ‘esoterisch’
  - Grote datasets
  - Eigen rechtenbeheer (wie mag bijdragen)
  - Niet perse openbaar
  - Eigen IT-hosting
* Met alle voordelen van Wikidata
  - Gericht op samenwerking en verbinding (o.a. Wikidata-community)
  - Voor mensen en machines
  - Gebruiksvriendelijke GUI voor gestructureerde data (Qs en Ps)
  - Ondersteuning voor meertaligheid
  - Versiegeschiedenis
  - Overzichtelijke ontologie: Items, Properties, Statements etc.
  - Output in diverse dataformaten (o.a. JSON, RDF/XML, N3)
  - Zoeken via SPARQL
  - MediaWiki API
  - Ondersteuning voor tools (o.a. OpenRefine)
  - Documentatie

<hr>
Wikibase website: https://wikiba.se/
Het grotere plaatje, Wikidata-Wikibase strategie: https://meta.wikimedia.org/wiki/LinkedOpenData/Strategy2021/Joint_Vision + https://meta.wikimedia.org/wiki/LinkedOpenData/Strategy2021/Wikibase 

<hr>

### Voorbeelden van instellingen/projecten die Wikibase gebruiken (1-6)

* Wikidata: https://www.wikidata.org/wiki/Wikidata:Main_Page 

* Rhizome Artbase : https://artbase.rhizome.org/wiki/Main_Page Rhizome = art organization in NYC - Artbase = archive of born-digital art 1983-present.) - First Wikibase instance outside of Wikimedia projects - https://artbase.rhizome.org/wiki/Query/example1 

* Enslaved.org: https://enslaved.org + https://lod.enslaved.org/wiki/Meta:Main_Page LOD platform containing ±1M records (people, events, places, and sources) related to the transatlantic slave trade 
 https://tech-news.wikimedia.de/en/2021/02/18/stories-of-the-enslaved-told-using-wikibase/ 
 
* FactGrid: https://database.factgrid.de/wiki/Main_Page 
 Open collaborative international Wikibase knowledge graph for historical research, 312 participants
 FactGrid projects, by era: https://database.factgrid.de/wiki/FactGrid:Projects 
 Paris to download: https://database.factgrid.de/wiki/FactGrid:Nineteenth_Century#Paris_to_download 
 All the houses and streets of Paris c. 1820 in a data set with geographic coordinates and administrative information free to download 
 SPARQL: All the houses and streets of Paris c. 1820 https://tinyurl.com/yf4fvrf7 + https://blog.factgrid.de/archives/2333 

* Aviation Safety Network: https://aviation-safety.net/about/ 
 Provides up-to-date, complete and reliable authoritative information on airliner accidents and safety issues. 
 The ASN Wikibase: https://aviation-safety.net/wikibase - updated regularly by a large user community and contains descriptions of more than 258,000 accidents involving light aircraft, military aircraft, helicopters, gyroplanes, gliders, hot air balloons and UAVs since 1905.

* EU Knowlegde Graph: https://linkedopendata.eu/wiki/The_EU_Knowledge_Graph Contains information about 1.9M projects financed by the EU and 700K beneficiaries of European projects - https://hal.archives-ouvertes.fr/hal-03353225/document + https://www.youtube.com/watch?v=PyBWo-ka9JU 
 Kohesio website: https://kohesio.ec.europa.eu - Frontend voor EU Knowledge Graph https://www.wikimedia.de/presse/european-commission-goes-open-source-new-project-kohesio-uses-wikimedias-software-wikibase/ 
 Verken bv EU-projecten in je buurt - 1.259 EU-projecten in Zuid-Holland - https://kohesio.ec.europa.eu/nl/?kaart%20regio=Nederland,Zuid-Holland,Q3119#mijn%20regio 

* Kunstmuseum API: https://api.kunstmuseum.nl/wiki/Kunstmuseum_API Wikibase om data voor websites Delftsaardewerk.nl, Van Gogh Worldwide en Aziatisch keramiek vanuit verschillende musea te importeren en te leveren via een centrale API.
 Delftsaardewerk.nl, Collectie Kunstmuseum Den Haag, object 0400098: https://delftsaardewerk.nl/bekijken/voorwerp/gemeentemuseum-den-haag/400098 + https://api.kunstmuseum.nl/wiki/Item:Q2559 
 
* DNB/GND: GND - Gemeinsame Normdatei, Integrated authority file for German speaking countries, 8 M authority records on persons, corporate bodies, subject headings, geographical names, works etc. https://www.dnb.de/EN/Professionell/Standardisierung/GND/gnd_node.html Wikibase as a second home for the GND - To collaboratively edit and maintain authority records for the entire GLAM field and digital humanities.
 https://tech-news.wikimedia.de/en/2020/03/04/wikibase-and-gnd/ + LA BIBLIOTECA PIATTAFORMA DELLA CONOSCENZA - Collaborativa, inclusiva, reticolare - 2021 (vanaf p 145)
 
* Wikibase @KB (internal) Acceptatie-Wikibase (in ontwikkeling) https://acc.emma.zbkb.nl/wiki/Main_Page 
 KB-Centsprenten en middeleeuwse handschriften https://acc.emma.zbkb.nl/wiki/Special:AllPages?from=&to=&namespace=120 
 https://acc.emma.zbkb.nl/wiki/Item:Q1004 

* Meer Wikibase-instanties
  - https://wikibase.world/wiki/Project:Home -- [List of WB instances](https://tinyurl.com/2jkres9t)
  - https://github.com/shigapov/wikibase-knowledge-graphs#awesome-wikibase-instances 

<hr>

### Wikibase projects in libraries
Wikibase is being evaluated by libraries as a tool to help them store and manage their structured data, as well as connect to the world of linked open data. 
* German National Library (DNB) 
* KB, national library of the Netherlands 
* National Library of France (more info) 
* National Library of the Czech Republic (more info) 
* National Library of Luxembourg (more info) 
* National library of Greece (more info) 
* The Smithsonian Libraries (more info) 

Meerdere bibliotheken hebben pilots, experimenten en evaluaties met Wikibase gedaan. Wat zijn hun bevindingen?
* OCLC, Project Passage: https://www.oclc.org/content/dam/research/publications/2019/oclcresearch-creating-library-linked-data-with-wikibase-project-passage-a4.pdf
* Bibliotheken VS, Use cases for institutional Wikibase instances: https://github.com/timothy-mendenhall/wikibase-use-cases/blob/master/UseCases-2020.md 
* DNB, GND meets Wikibase: https://wiki.dnb.de/pages/viewpage.action?pageId=147754828 + https://wiki.dnb.de/pages/viewpage.action?pageId=167019461
* DBN/BnF: Wikibase for Cultural Heritage and Academia, Perceived pros and cons of Wikibase as a solution - https://joinup.ec.europa.eu/sites/default/files/custom-page/attachment/2020-11/Parallel-track-4_B-Fischer_J-Thill_A-Angjeli%20final%20ppt.pdf
* TIB/NFDI (Duitsland): Examining Wikidata and Wikibase in the context of research data management applications: https://blogs.tib.eu/wp/tib/2022/03/16/examining-wikidata-and-wikibase-in-the-context-of-research-data-management-applications https://www.youtube.com/watch?v=RPMkuDxHJtI Wikidata and Wikibase as complementary research services for cultural heritage data: https://blogs.tib.eu/wp/tib/2022/03/17/wikidata-and-wikibase-as-complementary-research-services-for-cultural-heritage-data/
* TIB/NFDI (Duitsland): https://zenodo.org/record/7738424 + http://docs.google.com/spreadsheets/d/1FNU8857JwUNFXmXAW16lgpjLq5TkgBUuafqZF-yo8_I/edit?usp=share_link  

<hr>

### 1) WB componenten & architectuur 
Diefenbach et al (2021), “Wikibase as an Infrastructure for Knowledge Graphs: the EU Knowledge Graph” - https://hal.science/hal-03353225/document MariaDB = relationale MySQL DB BlazeGraph = RDF triple store Query service UI = SPARQL
WB architecture documentation: https://wmde.github.io/wikidata-wikibase-architecture 

### 2) Wikibase datamodel Hoe worden dingen in een Wikibase beschreven?
 Wikibase datamodel (simpel) : https://www.mediawiki.org/wiki/Wikibase/DataModel/Primer 
Amsterdam in de EU Knowlegde Graph, “Amsterdam is de hoofdstad van Nederland”. Triple: - Item: Nederland - https://linkedopendata.eu/wiki/Item:Q19  - Eigenschap: Hoofdstad - https://linkedopendata.eu/wiki/Property:P27 - Waarde: Amsterdam - https://linkedopendata.eu/wiki/Item:Q43
Opbouw datamodel: - Unieke identifier Q43 in https://linkedopendata.eu/wiki/Item:Q43 - Meertalige fingerprint: Label, Beschrijving, Aliases (Ook bekend als) - Statement: P32 + Q19 - Qualifier met P33 - Bronvermelding - Externe identifiers (P’s): Amsterdam in andere databases
Versiegeschiedenis: https://linkedopendata.eu/w/index.php?title=Item:Q43&action=history
Wikibase datamodel (conceptueel) : https://www.mediawiki.org/wiki/Wikibase/DataModel 

#### Andere datamodellen in Wikibase 
Wikibase heeft een eigen uniek datamodel, daar zitten beperkingen aan. 
In hoeverre kun je andere (door de KB gebruikte) datamodellen (RDA, schema.org) in een WB opnemen?
Literatuur over beperkingen datamodel Wikibase - https://wikidataworkshop.github.io/2022/papers/Wikidata_Workshop_2022_paper_9774.pdf - Wikidata’22: Wikidata workshop at ISWC 2022 - daniil.dobriy@wu.ac.at (D.Dobriy); axel.polleres@wu.ac.at (A. Polleres) - CC BY 4.0 – CEUR Workshop Proceedings, http://ceur-ws.org, ISSN 1613-0073 - Diefenbach et al (2021), “Wikibase as an Infrastructure for Knowledge Graphs: the EU Knowledge Graph” - https://hal.science/hal-03353225/document - Bergamin, G. (2022). Wikibase, or The search for the unicorn. JLIS.It, 13(3), 49–62. https://doi.org/10.36253/jlis.it-484
Oplossingsrichting door National Library of Greece (NLG) - http://www.rda-rsc.org/sites/all/files/NLG_Wikibase.pdf - https://www.youtube.com/watch?v=TPIS11QK8jI - Samenvatting door Marieke Moolenaar (KB), interne email, 21-8-2023
Analyse door Marieke Moolenaar: https://plein.kb.nl/thoughts/25980 + https://github.com/schemaorg/schemaorg/wiki/BlazeGraphSPARQLHowto  

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
 


