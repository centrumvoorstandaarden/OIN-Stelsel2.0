# Inleiding

Het OIN stelsel
---------------

In dit document beschrijven we het doel en de werking van het OIN Stelsel. Het OIN is gestart als een noodzakelijk onderdeel van de Digikoppeling Standaard en is inmiddels een veel gebruikt identificatienummer binnen en zeker ook buíten Digikoppeling. De regels van uitgifte en gebruik van het OIN staan beschreven in de *Voorwaarden Digikoppeling* en de *Gebruiksvoorwaarden Digikoppeling*. Daarnaast geeft Logius OIN’s en SubOINs uit en slaat de informatie hiervan op in het OIN register en ontsluit die met de *COR*, de Centrale OIN Raadpleegvoorziening. Dit geheel van regels en uitvoering noemen we het *OIN stelsel*.

Waarom dit document? 
---------------------

De Voorwaarden Digikoppeling en de Digikoppeling Gebruiksvoorwaarden hebben een juridisch karakter en beantwoorden waarschijnlijk niet elke vraag van gebruikers van een OIN. In dit document proberen we daarom de werking van het OIN stelsel met al haar facetten nader te beschrijven in de hoop die vragen te beantwoorden.

Aanleiding voor een nieuwe versie van dit document
--------------------------------------------------

Dit document is een update op een versie die Logius in 2016 heeft uitgebracht. De aanleiding was toen een inventarisatie van een aantal inmiddels gegroeide knelpunten met voorstellen voor de wijzigingen van de regels voor gebruik en uitgifte van OIN’s en SubOINS. Het document stond aan de basis voor de wijzigingen die in 2017 doorgevoerd.

In 2020 wil Logius de OIN regels opnieuw op punten aanpassen. Dit was meteen een mooie gelegenheid om het document bij te werken en in lijn te brengen met zowel de wijzigingen uit 2017 en de (nog te accorderen) wijzigingen van 2020.

Doel en scope van document
--------------------------

Dit document beschrijft het OIN-stelsel. Het OIN-stelsel bestaat uit de volgende bouwstenen:

- OIN- en SubOIN systematiek

- Centrale OIN Raadpleegvoorziening (incl. subOIN-register)

- Toelichting op de juridische voorwaarden en overeenkomsten

Historie van het OIN
--------------------

Bij de ontwikkeling van de Digikoppeling standaard in 2006 is besloten om de identificatie in de standaard te baseren op een uniek identificerend nummer van een overheidsorganisatie. [bron document "Evaluatie OIN uitgiftev2", 2010]

De behoefte aan een identificatienummer ontstond om een aantal redenen:

- Identificatie op basis van een nummer in plaats van een naam. Namen zijn moeilijk eenduidig te krijgen, door verschillende spellingen, afkortingen en hoofdletters;

- Stroomlijning en standaardisatie van identiteiten en autorisatie. Het was gewenst om *overheidsbreed* eensluidende afspraken te maken over niveaus van autorisatie en dus niveaus van identiteit;

[bron document "OIN alternatieven3", 2011]

**OIN en PKIoverheid**

Het nummer werd opgenomen in het PKIoverheidcertificaat - als inhoud van het attribuut Subject.serialNumber -  en werd daarnaast gebruik in de adressering van berichten.

Dit unieke nummer werd het OIN, het *Overheidsorganisatie Identificatie Nummer*. De KvK - beheerder van het Handelsregister (HR) - adviseerde om het nummer op het FI-nummer te baseren. In het Handelsregister waren echter in die tijd echter niet alle overheidsorganisaties opgenomen die in het kader van de elektronische overheid van belang waren. Zo hadden allerlei zelfstandige onderdelen van een ministerie, zoals de Belastingdienst en Douane, geen eigen FI-nummer. Voor het gebruik van Digikoppeling was echter afgesproken dat een organisaties én onderdelen van organisaties die berichten willen uitwisselen met een andere overheid, en daartoe zelfstandig contracten afsluiten, een identificerend nummer moeten krijgen, ook als dat onderdeel niet beschikt over een eigen FI-nummer. Afgesproken is dat Logius het OIN ging uitdelen. Op termijn zou dan mogelijk altijd met een FI-nummer gewerkt kunnen worden, wanneer al die zelfstandige onderdelen ook in het Handelsregister zouden worden opgenomen. [bron document "Evaluatie OIN uitgiftev2", 2010] 

**OIN en HRN**

Ook voor private organisatie was een nummer noodzakelijk voor digitale gegevensuitwisseling met de overheid. Het OIN stond toen nog voor
*Overheids*identificatienummer en liet niet toe dat ook deze partijen zich inschreven in het OIN register. Logius heeft daarom met de certificaatuitgevers aparte afspraken gemaakt om in het verplicht te gebruiken PKIoverheidcertificaat een nummer te laten opnemen volgens de structuur van het OIN.  Voor een private organisatie werd niet het RSIN gebruikt. maar haar KvKnummer.  Dit nummer kreeg de naam Handelsregisternummer (HRN).

In 2010 werd door de KvK door een wetswijziging het nieuwe Handelsregister in gebruik genomen, waarin meer overheidsorganen, zoals de ministeries, ingeschreven konden worden. Het door Logius onderhouden OIN register bleef daarnaast bestaan. Het register bevatte inmiddels naast in het HR ingeschreven organisatie ook registraties van organisatie-onderdelen en voorzieningen en overheidsorganisaties die zich niet kunnen inschrijven in het HR. In 2014 is een publiektoegankelijk website gelanceerd waarin iedereen het OIN van een organisatie kon opzoeken. 

**Aanpassing OIN regels in 2016**

In 2016 zijn na brede afstemming met gebruikers de regels verduidelijkt wie in aanmerking kwam voor een OIN en subOIN.  De onderbouwing van de regels zijn vastgelegd in het document [OIN stelsel v1](#inleiding). De spelregels van het OIN zijn vastgelegd in de [Voorwaarden Digikoppeling](https://docs.logius.nl/display/CVS/200421++Voorwaarden+digikoppeling+v1.09) en [Gebruikersvoorwaarden Digikoppeling](https://docs.logius.nl/display/CVS/200421+Gebruiksvoorwaarden+Digikoppeling+v1.09).
Sinds de wijziging van 2016 staat de afkorting voor OIN voor *Organisatie* Identificatienummer.

**Doorontwikkeling COR**

Logius heeft sinds 2017 een aantal wijzigingen doorgevoerd in de ontsluiting van het OIN register:

- in 2017 werd de OIN website hernoemd in en uitgebreid naar de Centrale OIN Raadpleegvoorziening (COR). De COR toont op de website naast de OIN's ook de HoofdOINhouder indien die aanwezig is.

- De aanduiding of de vermelde OIN voor eFacturatie gebruikt kon worden is verwijderd, op verzoek van Logius;

- in 2018 is op verzoek van een aantal organisaties een RESTful API toegevoegd waarmee het OIN register online bevraagd kan worden. De website bleef ongewijzigd;

- in 2019 is aan het OIN register een aantal identificerende nummers toegevoegd, de BG codes voor gemeente en de CBS codes voor Waterschappen en Provincies. Deze gegevens zijn enkel voor de API opvraagbaar.

**Nieuwe voorstellen in 2020**

- in 2020 dient Logius een voorstel in dat mogelijk maakt dat *privaatrechtelijke partijen met een publieke taak*  en *privaatrechtelijke partijen ten behoeve van (SAAS-)dienstverlening* aan hun publieke klanten SubOIN’s kunnen aanvragen.

- in 2020 wordt voor het UZI register prefix '00000009' gereserveerd

## Leeswijzer

De de structuur van dit document is gebaseerd op de TOGAF standaard - TOgaf staat voor The Open Group Architecture Framework- .

|Hoofdstuk|Inhoud|
|---|---|
|Architectuurvisie| beschrjft op hoofdlijnen het doel en de kaders van het OIN|
|Businessarchitectuur| beschrijft de wijzingen en de rollen in het OIN|
|ApplicatieArchitectuur| beschrijft de functies van de COR|
|Data Architectuur|beschrijft de structuur van het OIN en SUbOIN|
|Technologie-Architectuur| geeft een technische beschrijving van de COR en de hieraan gekoppelde systemen en bronnen|
|bijlage|Begrippenlijst|


# Architectuurvisie

Doel OIN
--------

Het organisatie-identificatienummer (OIN) is het identificatienummer voor niet-natuurlijke personen ten behoeve van het digitale berichtenverkeer met de overheid. De toekenning van het OIN is gebaseerd op identificatie van de aanvrager van het OIN middels het Handelsregister dan wel een ander aangesloten overheidsregister.

### Inleiding

Het Organisatie-identificatienummer (OIN), voorheen Overheidsidentificatienummer, is onderdeel van de Digikoppeling standaard. De standaard wordt gebruikt in elektronische berichtuitwisseling met en door de overheid. Het OIN is een twintigcijferig nummer dat een organisatie identificeert in het digitale berichtenverkeer. Digikoppeling verplicht de opname van het OIN in het PKIoverheid certificaat zodat systemen kunnen worden geïdentificeerd en geauthenticeerd. Daarmee is het OIN een randvoorwaarde voor veilig digitaal verkeer.

Een groot aantal voorzieningen van de digitale overheid maakt gebruik van het OIN. Dat gebeurt op verschillende manieren en met verschillende doeleinden: de identificatie, authenticatie en autorisatie van organisaties of organisatieonderdelen, en de routering van berichten naar organisaties,organisatieonderdelen of voorzieningen.

Gebruik van het OIN
-------------------

Het OIN-nummer wordt als identificerend nummer gebruikt in PKIoverheidcertificaten (authenticatie), in de adressering en routering van berichten, en in autorisatietabellen. Organisaties mogen het OIN of subOIN gebruiken voor identificatie van organisaties en organisatieonderdelen in het digitaal verkeer. Het overig gebruik van het OIN of subOIN betreft:

- Authenticatie

- Autorisatie

- Adressering

- Routering

Deze functies worden toegelicht in Bijlage B.

| **Functie**| **Definitie**| **Toelichting functie OIN** |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Identificatie (Identificeren)](http://www.noraonline.nl/wiki/Identificatie) | Het bekend maken van de identiteit van personen, organisaties of IT-voorzieningen. (Bron: *NORA 3.0 Principes voor samenwerking en dienstverlening)* | Het OIN of subOIN is het identificerende nummer voor organisaties t.b.v. digitaal verkeer met de overheid.|
| [Authenticatie (Authenticeren)](http://www.noraonline.nl/wiki/Authenticatie) | Het aantonen dat degene die zich identificeert ook daadwerkelijk degene is die zich als zodanig voorgeeft: ben je het ook echt? Authenticatie noemt men ook wel verificatie van de identiteit. (Bron: *NORA 3.0 Principes voor samenwerking en dienstverlening)* | Het OIN of subOIN wordt opgenomen in het subject serialNumber veld van het PKIoverheid certificaat. |
| [Autorisatie (Autoriseren)](http://www.noraonline.nl/wiki/Authenticatie) | Het proces van het toekennen van rechten voor de toegang tot geautomatiseerde functies en/of gegevens in ICT voorzieningen.| Het feit dat een organisatie over een OIN of subOIN beschikt zegt niets over enige autorisatie op gegevens of informatie. Dit is voorbehouden aan de verstrekkende partij die dit zelf beoordeelt. Partijen die voorzieningen aanbieden kunnen zelf autorisatielijsten bijhouden waarin het OIN van geautoriseerde organisaties kan worden opgenomen. |
| **Adresseren** | Het aangeven van de ontvangende partij (en de verzendende partij) in het bericht.| Digikoppeling schrijft b.v. voor dat het OIN of subOIN wordt gebruikt in de header voor adressering.|
| **Routeren** | Het doorsturen van een bericht aan de geadresseerde partij bijvoorbeeld via een routeringsregel of tabel.| Routering vertaalt het logische adres – het OIN of subOIN – naar een fysiek endpoint (url). |

Context Centrale OIN Raadpleegvoorziening (COR)
-----------------------------------------------

In onderstaand diagram wordt de relatie tussen COR met de omgeving weergegeven.

![\_scroll_external/attachments/contextdiagram-v5-30b44b85ba71eac7302e30a1e137f91c735ce0c67fce59af559deb4f9ce5b0fa.jpg](media/289487c16471f3a60096389e7e51e2fa.jpg)

 
*Figuur 1 Context diagram OIN-raadpleegvoorziening en OIN spelregels*

Kaders en bronnen
-----------------

De volgende kaders en bronnen zijn gehanteerd bij de uitwerking van het OIN-stelsel:

- NORA is het kader voor de uitwerking van de Centrale OIN Raadpleegvoorziening.

- Memo OIN: *Gebruik van OIN, knelpunten en oplossingen Het memo met opleggers zijn op aangeboden aan de Regieraad Gegevens van 14 januari 2016. De stukken
zijn schriftelijk besproken. De stukken zijn te vinden op* <https://digitaleoverheid.pleio.nl/file/group/30207952/all#41536872>

- *200421 Voorwaarden Digikoppeling v1.09.docx:* conceptversie metwijzigingsvoorstellen voor verruiming van het beleid van SubOIN uitgifte
voor afnemers.

- 200421 Gebruiksvoorwaarden Digikoppeling v1.09 conceptversie met wijzigingsvoorstellen voor verruiming van het beleid van SubOIN uitgifte
voor gebruikers.

# Businessarchitectuur

Wat is het OIN 
---------------

Het Organisatie-identificatienummer (OIN) is een uniek nummer dat Logius kan toekennen aan organisaties om zich te kunnen identificeren, authentiseren en of autoriseren bij digitaal berichtenverkeer binnen en met de overheid.

Voor wie is het OIN 
--------------------

Het OIN is voor organisaties die berichten uitwisselen met de overheid. Dit kunnen publieke en private organisaties zijn. Voorwaarde is dat zij staan ingeschreven in het handelsregister. Daarnaast kunnen ook een aantal organisaties die niet in het handelsregister zijn opgenomen een OIN aanvragen. Dit zijn bijzondere organisaties met een publieke taak, colleges van advies en internationale organisaties met een rechtspersoonlijkheid.

Het OIN maakt een onderscheid in gebruikers en afnemers. Beiden kunnen het OIN aanvragen. Deze begrippen komen uit de *Algemene Voorwaarden Logius voor afnemers* en zijn als volgt gedefenieerd

- Afnemer: een publiekrechtelijke of privaatrechtelijke organisatie, ofcollege of een persoon met een publieke taak of bevoegdheid, die voor de uitoefening van die publieke taak elektronisch verkeer met andere overheden en burgers en/of bedrijven wenselijk acht en daarbij gebruik kan en mag maken van één of meer Diensten van Logius.

- Gebruiker: een overheidsorganisatie of; onderneming of een rechtspersoon, die is ingeschreven in het Handelsregister of; natuurlijk persoon die is ingeschreven in de Gemeentelijke Basisadministratie persoonsgegevens (GBA), en in deze hoedanigheid gebruik maakt van de Diensten van Logius ten behoeve van het elektronisch verkeer met één of meerdere Afnemers.

Op welke manier kan een organisatie een OIN verkrijgen
-------------------------------------------------------

Bedrijven en privaatrechtelijke instellingen die digitaal communiceren met de overheid hebben daarvoor in veel gevallen een identificerend nummer nodig. Dit identificerende nummer kan op twee manieren verkregen worden:

1.Bij Logius: Door een OIN (Organisatie Identificatie Nummer) aan te vragen bij Logius via een aanvraagformulier op Logius.nl. Het OIN wordt afgeleidvan het KvK-nummer uit het Handelsregister. Het OIN wordt vastgelegd in een register dat publiek raadpleegbaar is via de centrale OIN Raadpleegvoorziening (<https://portaal.digikoppeling.nl/registers/>) via een website en een API. De regels uit de Gebruiksvoorwaarden Digikoppeling (versie 2?) zijn van toepassing. Er zijn geen kosten verbonden aan deze registratie.

2.Bij de TSP: Bij de aanvraag van een PKIoverheid-certificaat zal de Trust Service Provider (TSP), bij ontbreken van een OIN, het identificerend nummer bij de creatie van het certificaat zelf afleiden op basis van het KvK-nummer uit het Handelsregister op gelijke wijze als bij de afleiding van het OIN. Er vindt echter geen publiek raadpleegbare registratie plaats. Voor de werking van het dataverkeer met de overheid is er verder geen verschil.

Wat is een SubOIN
------------------

Het SubOIN is een afgeleide van het OIN, volgens dezelfde nummersystemathiek, voor die onderdelen van de organisatie die geen rechtspersoon zijn maar wel een uniek inditificatinummer behoeven voor digitale communicatie met de overheid. Juridisch zijn die organisatieonderdelen altijd onderdeel van de organisatie die het bovenliggende OIN heeft verkregen.

Voor wie is het SubOIN
-----------------------

Het SubOIN is aan te vragen door organisaties die voor het uitvoeren van een publieke taak behoefte hebben aan een identificerend nummer op het niveau van organisatieonderdelen.

Daarnaast is het SubOIN aan te vragen door partijen die als onderdeel van hun dienstverlening aan overheden (of publieke organisaties) een uniek
identificerend nummer nodig hebben en het OIN nummer hiervoor niet kunnen gebruiken.

Wijzigingen in het OIN Stelsel sinds 2006 
------------------------------------------

Sinds het onstaan van het OIN is een aantal wijzigingen doorgevoerd in de toekenning en het gebruik van het OIN. De belangrijkste wijzingen geven we hieronder weer:

In 2017 zijn - naast duidelijker uitgeschreven juridische kaders- de volgende aanpassingen in de OIN regels uitgevoerd:

- de mogelijkheid voor organisaties met publieke rechtspersoonlijkheid om SubOIN’s aan te vragen voor aan hen gerelateerde organisatieonderdelen, voorzieningen en samenwerkingsverbanden

- de mogelijkheid voor houders van sectorregistraties om op te gaan treden als SubOIN-beheerder en op die manier door hen geregistreerde organisaties die geen eigen (Nederlandse) rechtspersoonlijkheid bezitten ook van SubOIN’s te voorzien.Voor identificatie

- private partijen, die staan geregistreerd bij de KvK, krijgen de mogelijkheid om zich ook te laten registreren in de COR waarbij er een OIN
afgeleid wordt van het KvK-nummer toegekend en de organisatiegegevens vanuit het Handelsregister worden overgenomen.

- Met het doorvoeren van het nieuwe beleid is het begrip OIN van *Overheids* IdentificatieNummer gewijzigd naar *Organisatie* IdentificatieNummer.

In 2017 verving de COR het toenmalige OIN register. Aan de COR werden de volgende nieuwe functionaliteiten toegevoegd:

- De relatie tussen SubOIN’s en de verantwoordelijke rechtspersoon kan in de COR worden vastgelegd en wordt publiekelijk getoond bij raadpleging van de voorziening.

- De mogelijkheid tot aanmaak, wijziging en intrekking van SubOIN’s door beheerders is toegevoegd.

- Beheerders hebben de mogelijk gekregen om de organisatiegegevens behorend bij een OIN rechtstreeks vanuit het Handelsregister via de KVK-API op tevragen en in de COR over te nemen waarmee de kwaliteit van geregistreerde gegevens kan worden verhoogd zonder extra benodigde handmatige handelingen.

- De exportfunctionaliteit waarmee de inhoud van de COR-database in CSV-formaat kan worden gedownload is publiek beschikbaar gemaakt.

- Beheerders hebben de mogelijkheid gekregen om de relatie met een SubOIN van de ene rechtspersoon naar een andere rechtspersoon over te dragen. Dit komt van pas als er een organisatieonderdeel of voorziening overgaat van de ene instantie naar een andere.

- Het al dan niet kunnen gebruiken van (Sub)OIN’s voor e-facturatie wordt publiekelijk getoond.

- Niet alleen actieve (Sub)OIN’s maar ook ingetrokken (Sub)OIN’s worden publiekelijk getoond.

- Er is een voorziening aangebracht waarmee het aantal bevragingen van de COR kan worden gerapporteerd

De COR is sinds de lancering steeds verder doorontwikkeld en aangepast;

- het eFacturatie kenmerk wordt niet meer getoond in de COR. Deze informatie over is nu te vinden op [https://www.logius.nl/diensten/e-factureren](https://www.logius.nl/diensten/e-factureren)

- Restful API op de COR: de COR API biedt verschillende mogelijkheden om het OIN register te bevragen

- extra identificerende codes toegevoegd aan het OIN register. Hierdoor is het mogelijk om via de COR API de vertaling te maken van OIN naar Gemeentecode en omgekeerd. Naast Gemeentecode kan een vertaling worden opgevraagd naar Provincie-, Waterschap- of Ministeriecode

Het gebruik van het OIN neemt steeds meer toe. Hierdoor zijn nieuwe knelpuntenin de praktijkonstaanwaarbij de OIN spelregels knelden met de behoefte en noden van organisaties.

In 2020 legt Logius een aantal wijzigingsvoorstellen in de OIN spelregels aan de Digikoppeling Community. De nieuwe spelregels
zijn verwerkt in de aange[aste *Voorwaarden Digikoppeling* en *Gebruiksvoorwaarden Digikoppeling*.

Belangrijkste wijzigingen 

- Private partijen met een publieke taak kunnen SubOIN’s kunnen aanvragen;

- Private partijen kunnen ten behoeve van (SAAS-)dienstverlening aan hun publieke klanten SubOIN’s aanvragen

Daarnaast zijn de Voorwaarden verduidelijkt en up-to-date gebracht. Voor het OIN gaat het om de volgende onderdelen:

- Geen vermelding meer tbv e-factureren in de COR

- Vermelding van het gebruik van organisatiecodes in de COR

Rollen in het OIN stelsel
-------------------------

### Stakeholders

Stakeholders bij het gebruik van het OIN-Stelsel zijn in beginsel alle partijen die gebruik maken van het (sub)OIN en/of bijbehorende centrale OIN register
(COR) én de partijen die een rol hebben bij het beheer van het OIN.

### Opdrachtgever

Het ministerie van BZK (BZK) is opdrachtgever van Logius en eigenaar van het OIN-stelsel. Als eigenaar draagt BZK ook verantwoordelijkheid voor toezicht en audits over de centrale voorziening en afspraken.

### Beheerder OIN-stelsel

Logius beheert het OIN Stelsel. Het OIN valt onder de Digikoppeling Standaard. Het Centrum voor Standaarden, van Logius is beheerder van de Digikoppeling standaard en voert ook het beheer over van het OIN-stelsel, voorwaarden en overeenkomsten.

### Beheerder COR

Logius beheert de Centrale OIN Raadpleegvoorziening (COR). Logius Team Interfaces, onderdeel van het Productiehuis van Logius voert het dagelijks beheer en de doorontwikkeling uit van de COR.  Logius heeft de zorgplicht om de COR online toegankelijk te houden voor de gebruikers van de COR.

### Registerhouder overheidsregister

De registerhouder beheert een overheidsregister en waarborgt de kwaliteit van de te raadplegen nummers en bijbehorende gegevens. Voor elke entiteit die is opgenomen in het overheidsregister is duidelijk wie de verantwoordelijke rechtspersoon is. De verantwoordelijke rechtspersoon is herkenbaar aan de hand van het identificerende nummer (RSIN, KvK nummer of OIN). Het register heeft geborgd dat als de rechtspersoon ophoudt te bestaan, de registratie van de entiteit vervalt.

### SubOIN-beheerder

Een overheidsorganisatie kan na invulling van het aansluitformulier en toetsingprocedure door de COR beheerder toegelaten worden alsSubOIN-beheerder. De SubOIN-beheerder draagt zorg voor de registratie van SubOIN's voor organisaties die niet in een aangesloten register voorkomen maar die wel bij een broninstantie of op basis van brondocumenten kunnen worden geïdentificeerd en geverifieerd. De SubOIN-beheerder stelt de identificatie van een buitenlandse partij vast aan de hand van bewijsstukken of zelfstandig onderzoek. Een SubOIN-beheerder kan eenSubOIN aanmaken voor specifieke partijen die niet in het Handelsregister staan maar wel identificeerbaar moeten zijn. De
identiteit van de aanvrager moet door de SubOIN-beheerder worden gecontroleerd aan de hand van brondocumenten of andere bronnen. De SubOIN-beheerder kan SubOIN's aanmaken en publiceren of intrekken via de COR. De SubOIN-beheerder is verantwoordelijk voor het doorvoeren van mutaties.

### Certificatiedienstverlener (TSP)

De TSP's geven certificaten uit conform de eisen uit het PvE van PKIoverheid.Daarmee zijn zij verantwoordelijk voor de betrouwbaarheid van de genoemde certificaten. De TSP's doen met het oog op het uitgeven van een certificaat onderzoek naar de identiteit van de organisatie en de tekenbevoegdheid *De voorwaarden hiervoor zijn beschreven in het PvE PKIo PvE (deel 3 aanvullende eisen)* van de aanvragers van een certificaat. Tevens controleren zij de identiteit van de aanvrager op grond van een face to face controle. De TSP raadpleegt het OIN van de aanvrager via de COR en neemt dit nummer en naam op in het PKIoverheid certificaat.

### OIN-houder

De OIN-houder is een rechtspersoon met een publieke taak, die gebruik maakt van het OIN. Slechts een OIN–houder kan een SubOIN aanvragen voor een organisatie, organisatie-onderdeel of voorziening die onder zijn juridische verantwoordelijkheid valt.

### Beheerder PvE PKIoverheid

Logius PKIoverheid is beheerder van het Programma van Eisen van PKIoverheid en toezichthouder op de TSP's.

Juridische structuur
--------------------

Aansluitend op de beschrijving en uitleg van de rollen van betrokken partijen in het vorige hoofdstuk worden de kernbegrippen in de juridische context toegelicht.

Er van uitgaande dat het OIN voorlopig geen wettelijke grondslag krijgt zijn de Voorwaarden Digikoppeling en de OIN-formulieren de aangewezen plaats om de spelregels voor de betrokken partijen te definiëren. 

### OIN-voorwaarden en OIN–formulieren

Onderstaand schema beschrijft op welke manier organisaties een OIN of SubOIN bij Logius kunnen aanvragen

![\_scroll_external/attachments/image2020-6-30_13-46-43-22c5c4b15c5628a3682e5a48c5cd72e4522ff503bb08574009d456d68ab329a8.png](media/f8c0729b1928e3d6968bc669bf9b67ca.png)

Figuur 2: Juridische instrumenten (onderdeel van Digikoppeling)

### Identificatie

Het gebruik van een Organisatie Identificatienummer (OIN) beoogt rechtspersonen en niet-rechtspersonen te identificeren ten behoeve van digitale
berichtenverkeer met de overheid.

### Handelsregister

Een OIN is waar mogelijk afgeleid van bestaande identificerende nummers uit het Handelsregister.

### Rechtspersonen en samenwerkingsverbanden

Rechtspersonen en samenwerkingsverbanden *Dit zijn de samenwerkingsverbanden die zich conform de Hrw in kunnen schrijven in het Handelsregister.* worden ex art.6 Handelsregisterwet (Hrw) ingeschreven in het Handelsregister, en kunnen dus worden geïdentificeerd ten behoeve van het gebruik van het OIN. Tevens kunnen de in art. 1:2 Algemene wet bestuursrecht (Awb) omschreven overheidsorganen, die niet in het Handelsregister kunnen worden ingeschreven, een OIN verkrijgen.

### Buitenlandse rechtspersonen en organisaties

Buitenlandse rechtspersonen en organisaties die niet ingeschreven kunnen worden in een Nederlands overheidsregister, maar wel voldoen aan de vereisten voor een PKIoverheidscertificaat, kunnen bij een SubOIN-beheerder een aanvraag indienen voor een OIN. Na controle door een SubOIN-Beheerder kunnen deze buitenlandse organisaties een SubOIN krijgen.

SubOIN
------

Organisaties, organisatieonderdelen en/of voorzieningen die niet in een aangesloten overheidsregister voorkomen, komen mogelijk toch in aanmerking voor een SubOIN. (In enkel bijzondere gevallen ook voor een OIN. Het gaat dan om het OIN dat wordt toegekend aan een onderdeel van de Staat der Nederlanden). Deze worden geregistreerd in het SubOIN-register. Een SubOIN is een identificerend nummer voor niet-rechtspersonen. Het SubOIN heeft dezelfde structuur als het OIN. Een SubOIN is altijd herleidbaar tot een rechtspersoon die is ingeschreven in het Handelsregister en valt onder de juridische verantwoordelijkheid van deze rechtspersoon.

### OIN-houder

De OIN-houder is een rechtspersoon met een publieke taak die gebruik maakt van het OIN. Slechts de OIN–houder kan een SubOIN aanvragen voor een organisatie, een organisatieonderdeel of een voorziening die onder zijn juridische verantwoordelijkheid valt. De OIN-houder zal zich ervan moeten vergewissen dat hij middels juridische afspraken – zoals bijvoorbeeld statuten, een overeenkomst, een inschrijving in een register en/of een mandaatbesluit – juridische verantwoordelijkheid kan dragen voor het handelen van de organisatie of organisatieonderdeel, die gaat beschikken over een SubOIN Een eis is dat de functionaris, die de aanvraag voor een SubOIN doet, tekenbevoegd is.

De OIN–houder heeft een zorgplicht met betrekking tot het handelen door de houder van het SubOIN, voor zover dit handelen betrekking heeft op de elektronische berichtenuitwisseling waarbij gebruik wordt gemaakt van het OIN en bijbehorende SubOIN's.

### SubOIN op basis van een aangesloten register

Als een organisatie geregistreerd is in een aangesloten register (niet het Handelsregister), dan kan het identificerend nummer uit dit register worden gebruikt als SubOIN. Daarmee is een aangesloten register in feite een register van SubOIN's voor een specifieke doelgroep.

### Opnemen OIN in PKIoverheidscertificaat

De TSP neemt een OIN of SubOIN op in een PKIoverheidscertificaat. Hiervoor wordt het *Subject.serialNumber* veld van het certificaat gebruikt.

 Centrale OIN Raadpleegvoorziening (COR)
----------------------------------------

Logius is beheerder van de Centrale OIN Raadpleegvoorziening (inclusief het SubOIN-register) in opdracht van BZK. De nieuwe COR heeft niet het karakter van een basisregistratie of een sectorale registratie. De COR is een landelijke voorziening.

Toezicht uitoefenen
-------------------

Logius moet toezien op de naleving van de voorwaarden en de afspraken die partijen met Logius maken.Logius moet voldoen aan de kwaliteitseisen vanuit haar opdrachtgever BZK. Daarbij is de mogelijkheid aanwezig dat BZK onafhankelijke derden, zoals de ADR *Auditdienst Rijk*, inschakelt om controles uit te voeren. Daarmee is de functiescheiding gewaarborgd.

### Naleving Voorwaarden OIN

De beheerder van het OIN-stelsel controleert op basis van signalen en steekproefsgewijs de naleving van de OIN-voorwaarden en de ondertekende
aanvraagformulieren met de OIN–houders, die SubOIN's uitgeven.

### Naleving overeenkomsten

De beheerder van het OIN-stelsel controleert de naleving van de overeenkomsten, af te sluiten met de SubOIN-beheerders en met de registratiehouders.

### Toezicht BZK

De opdrachtgever BZK beoordeelt binnen het regulier toezicht op de beheerder van het OIN-stelsel in hoeverre de OIN-voorwaarden en overeenkomsten nageleefd worden door de betrokken contractspartijen.

Internationale uitwisselingen
-----------------------------

Voor internationale uitwisselingen is alleen het gebruik van het OIN niet voldoende. Er ontbreken dan twee elementen die in internationaal verband nodig zijn:

1.Volgens de ISO 6523 part 1 standaard is een ICD code nodig. Het OIN is sinds 2018 opgenomen in de ICD lijst

2.Voor gebruik binnen de EU wordt een EU ID verplicht. Dit EU ID onderkent een landcode; de impact van het EU ID moet nog worden onderzocht.

De volgende alinea's geven achtergrondinformatie over de ISO 6523 standaard, het EU ID en het gebruik van de ISO landcode.

### Mapping naar de ISO 6523 standaard

Het OIN is aangemeld en opgenomen in in ICD Codelist: <https://docs.peppol.eu/poacc/billing/3.0/codelist/ICD/>

Het OIN is geregistreerd onder code id 0190 me de volgende beschrijving

Organisatie Indentificatie Nummer (OIN)

> The OIN is part of the Dutch standard ‘Digikoppeling’ and is used for identifying the organisations that take part in electronic message exchange with the Dutch Government. The OIN must also be included in the PKIo certificate.

# Applicatie-architectuur

Gebruik van de Centrale OIN Raadpleegvoorziening
------------------------------------------------

Het OIN van een rechtspersoon is publiek raadpleegbaar via de Centrale OIN Raadpleegvoorziening (COR). De COR registreert organisaties en stelt het OIN samen op basis van de OIN-systematiek (zie bijlage A). Voor de registratie baseert de COR gebruikt zich waar mogelijk op registers met een wettelijke of formele taak, zoals het Handelsregister en het FI register. De gebruiker kan in de COR zoeken op nummer of naam. De zoekresultaten worden aan de gebruiker getoond. 

De COR is sinds 2017 als publiek toegankelijke voorzienig beschikbaar.

De COR bestaat uit de volgende kern-onderdelen:

- Een publiek toegankelijk raadpleegvoorziening.

- Een webservice die een Restful API aanbiedt

- Een beheermodule waarmee Logius beheerders de COR content bijhouden.

Publieke raadpleegvoorziening
-----------------------------

De COR biedt de volgende services voor gebruikers:

- Online zoeken naar OIN en SubOIN op basis van nummers, organisatienamen ofdelen ervan

- REstful API functionaliteit

- Export van alle geregistreerde organisaties in CSV formaat

Beheerfuncties
--------------

De COR biedt, naast bovenstaande, de volgende services voor beheerders:

- Detailinformatie over de geregistreerde organisaties en een bewerkmogelijkheid om deze informatie aan te passen

- Historie/audittrail van alle doorgevoerde wijzigingen per registratie

- Mogelijkheid om nieuwe OIN- en SubOIN-registraties toe te voegen

- Mogelijkheid om actieve OIN en SubOIN's in te trekken

- Data synchronisatie tussen de COR database en het Handelsregister. zowel bij invoer van nieuwe registraties als periodiek, om bestaande registraties te verifiëren

- Lifecycle management van SubOIN's

- Gebruikersbeheer

Algemene eisen aan de Centrale OIN Raadpleegvoorziening
-------------------------------------------------------

De Centrale OIN Raadpleegvoorziening voldoet aan de volgende eisen:

- De authenticatie van beheerders verloopt via een beveiligd authenticatiemiddel.

- Er is een systeemcontrole die voorkomt dat er duplicaten van OIN's of SubOIN's ontstaan.

- Er is een systematiek(algoritme) voor het genereren van een uniek nummer die gaat dienen als SubOIN.

- De beheerder treft passende beveiligingsmaatregelen om de privacy van de verwerking van persoonsgegevens te waarborgen, zoals de Logiusbeveiligingsrichtlijnen (ISO27000-1 en ISO 27000-2) en IB policies.

- Maakt gebruik van Nederlandse API Design Rules voor webservice.

- Voorziet in een audittrail van mutaties op een registratie.

- Voorziet in management rapportages die inzicht bieden in aantallen SubOIN's, gebruikers, activiteiten OIN-houders enzovoort.

- Voldoet aan Digitoegankelijk

- Volgt de principes en kaders van NORA.

- Voldoet aan de eisen die gesteld worden door de beheerders van overheidsregisters.

SubOIN's: uitgifte
------------------

### Regels voor uitgifte SUbOIns

**Aanmaken SubOIN**

Een rechtspersoon, die OIN–houder is, kan een SubOIN aanvragen voor een entiteit zonder rechtspersoonlijkheid - te weten een organisatie, organisatieonderdeel of voorziening - waarvoor hij de juridische verantwoordelijkheid neemt voor het gebruik van SubOIN's. De SubOIN's worden beheerd in het *SubOIN-register*, onderdeel van de COR. Onder de definitie van een entiteit vallen ook diensten zoals (landelijke) voorzieningen, mits deze als een onderdeel van een organisatie beschouwd kunnen worden en geïdentificeerd moeten worden voor informatie-uitwisseling. Logius maakt op verzoek van een OIN-houders SubOINs aan in de COR.

Organisaties in andere registers dan het Handelsregister

Organisaties die geregistreerd staan in andere aangesloten registers dan het Handelsregister worden beschouwd als houders van een SubOIN. Voor deze organisaties gelden dezelfde regels als houders van SubOIN die door rechtspersonen zijn aangemaakt.

### Aanvragen PKIoverheidscertificaat

De OIN–houder vraagt een PKIoverheidscertificaat aan ten behoeve van identificatie/authenticatie, signing of encryptie. De TSP verstrekt het PKIoverheidcertificaat aan de houder van het OIN. Als een PKI Overheid certificaat wordt aangevraagd door de OIN-houder ten behoeve van een SubOIN-houder, dan neemt de TSP daarin het SubOIN op en de bijbehorende naam uit het SubOIN-register.

### Samenwerkingsverbanden

Een deelnemer binnen een (publiek) samenwerkingsverband zonder rechtspersoonlijkheid mag een SubOIN uitgeven aan het samenwerkingsverband, mits de betreffende deelnemer OIN-houder is. De deelnemers dienen onderling te borgen dat de aanvrager is gemandateerd om een aanvraag te doen namens de overige deelnemers.

SubOIN's: beheer
----------------

### Mutaties doorgeven aan de COR

De OIN–houder moet alle mutaties met betrekking tot de SubOIN's doorgeven aan Logius, beheerder van de COR.

### Intrekkingsplicht

De OIN–houder is verplicht een SubOIN in te trekken in de COR, indien het voor frauduleus handelen kan worden of wordt gebruikt, of de betreffende organisatie of organisatieonderdeel ophoudt te bestaan of overgaat naar een andere organisatie of rechtspersoon. Daarnaast beschikken de SubOIN-beheerders en Logius over de bevoegdheid tot het intrekken van SubOIN's.

### Beheerder van een overheidsregister

De beheerder van een overheidsregister borgt dat wijzigingen worden gecontroleerd en worden doorgevoerd zodat een SubOIN alleen kan worden gebruikt zolang de registratie in het overheidsregister geldig is en de rechtspersoon bestaat. Het SubOIN van de entiteit is altijd herleidbaar tot de juridisch verantwoordelijke rechtspersoon.


SubOIN's: geldigheidsduur en bewaartermijnen
--------------------------------------------

### Geldigheidsduur

De door de OIN-houder uitgegeven SubOIN's hebben een geldigheidsduur van drie jaar. SubOIN's kunnen worden verlengd door de OIN-houder via een verzoek aan Logius.


### Beëindigen

Als het KvK-nummer of RSIN vervalt, vervalt het OIN. Als het OIN vervalt, mogen de daaraan gerelateerde SubOIN's niet meer worden gebruikt, en moeten deze worden ingetrokken.

Centrale OIN Raadpleegvoorziening (COR)
---------------------------------------

### Onderdelen van de COR

De COR bestaat uit een publiek toegankelijk gedeelte en een besloten gedeelte. Het publiek toegankelijke deel wordt ontsloten door een website en een webservice met een Restful API.

### Toegang tot het besloten gedeelte van de COR

Enkel daarvoor aangewezen medewerkers van Logius hebben toegang tot het besloten gedeelte van de COR.

### Registratie in het besloten gedeelte van de COR

De rechtspersoon of SubOIN-beheerder registreert in het besloten gedeelte van de COR:

- Het uitgeven van een nieuw SubOIN.

- Het intrekken van een bestaand SubOIN.

- Het verlengen van de geldigheidsdatum van een SubOIN

- Het verlengen van SubOIN die was ingetrokken na de standaard geldigheidsduur

- Wijzigingen in de registratie van organisatie(onderdelen) of voorzieningen.

### Publiceren SubOIN

Het SubOIN is pas openbaar toegankelijk, nadat de OIN-houder (rechtspersoon met publieke taak) of SubOIN-beheerder het SubOIN heeft gepubliceerd.

| **todo** Website en CORAPI publiceren ook de ingetrokken OINs |
|---------------------------------------------------------------|


### Aansluiten COR op overheidsregisters

De beheerder van het OIN-stelsel bepaalt welke overheidsregisters onderdeel uitmaken van de OIN-systematiek. De beheerder van het OIN-stelsel maakt afspraken over het gebruik van deze registers met de registratiehouders. De registratiehouders zijn verantwoordelijk voor de kwaliteit van gegevens en voor de beschikbaarheid van het register.

### Gebruik van de COR webservice

De COR webservice is publiek beschikbaar voor systemen. Logius kan de toegang reguleren, bijvoorbeeld door het verstrekken van zogenaame API-keys, of gebruikt te maken van tweezijdig TLS. 

### Privacybescherming en informatiebeveiliging

De beheerder van de COR is verantwoordelijk voor de privacybescherming van persoonsgegevens in de COR en de informatiebeveiliging met betrekking tot de COR, en komt derhalve de van toepassingzijnde wet – en regelgeving na.

### Kwaliteitsborging

De beheerder van de COR is verantwoordelijk voor het technisch functioneren van de COR en voor het bieden van ondersteuning bij het gebruik van de COR. De beheerder van de COR zorgt voor de beschikbaarheid van het systeem. Deze afspraken worden vastgelegd in een Service Level Agreement.De beheerder van de COR is niet verantwoordelijk voor de kwaliteit van de SubOIN's. De rechtspersonen die de SubOIN's uitgeven hebben een zorgplicht met betrekking tot de inhoud van de geregistreerde gegevens in de COR. Bij twijfel over de juistheid van geregistreerde gegevens kan de beheerder van de COR maatregelen nemen om de kwaliteit van subnummer registraties te toetsen en desgewenst te herstellen. De beheerder van de COR is niet verantwoordelijk voor de kwaliteit van de gegevens uit de aangesloten overheidsregisters.

Aanvraagformulieren
-------------------

De OIN–houder die SubOIN's aanvraagt voor organisatie(s) of organisatieonderdelen, zal het aanvraagformulier moeten invullen en ondertekenen. Daarop zijn ook de Voorwaarden Digikoppeling en de Gebruikersvoorwaarden van toepassing. De spelregels uit dit document worden opgenomen binnen de aan te passen voorwaarden.De OIN–houder verklaart zich op het formulier juridisch verantwoordelijk voor het gebruik van het SubOIN door de houder van het SubOIN. 

# Data-architectuur

OIN: samenstelling en raadpleging
---------------------------------

Het OIN wordt samengesteld op basis van een inschrijving in het Handelsregister of ander (op de COR) aangesloten overheidsregister. Organisaties die geregistreerd staan in een ander aangesloten register beschikken daarmee over een SubOIN. Het OIN kan publiekelijk worden geraadpleegd via de COR. De COR raadpleegt de aangesloten overheidsregisters en stelt het OIN samen op basis van de OIN-systematiek zoals beschreven in bijlage A.

### Registerhouders van overheidsregisters

Logius maakt afspraken met registerhouders over het gebruik van overheidsregisters ten behoeve van het kunnen raadplegen van deze registers via
de COR.Registers kunnen worden aangesloten op het OIN-stelsel indien ze voldoen aan de volgende voorwaarden:

- Er is een juridische grondslag voor het register.

- Er is een beheerder die het inhoudelijk en technisch beheer voert.

- De beheerder controleert de identiteit van de rechtspersoon aan de hand van
het Handelsregister.

- Het identificerende nummer is gekoppeld aan een rechtspersoon.

- Het overheidsregister is publiek raadpleegbaar.

- Er is een webservice beschikbaar.

Samenstelling OIN
-----------------

De lengte van het OIN is 20 posities, omdat dit wordt opgenomen in het *subject serial number* field van het PKIoverheid certificaat; dit veld bestaat uit 20 posities.De OIN-systematiek blijft ongewijzigd. Het OIN is opgebouwd uit de volgende elementen:

| **Element** | **Lengte**| **Waarde**|
|-----------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Prefix**| 8 posities| Zie Prefix tabel|
| **Hoofdnummer** | 8 of 9 posities | Identificerend nummer *Dit kan ook alfanumeriek zijn, afhankelijk van het geraadpleegde register.* uit een register. Als het hoofdnummer een KvK nummer is, is het hoofdnummer 8 posities lang. |
| **Suffix**| 3 of 4 posities | Als het hoofdnummer 9 posities heeft dan is het suffix 000. Als het hoofdnummer 8 posities heeft dan is het suffix 0000.|

Samenstelling SubOIN
--------------------

Een SubOIN is een *betekenisloos* nummer dat wordt gegeneerd tijdens de registratie. Betekenisloos houdt in dat het SubOIN zelf geen aanwijsbare relatie heeft met het OIN van de OIN-houder. De relatie is alleen te raadplegen via de COR. Een SubOIN is een OIN voor entiteiten zonder rechtspersoonlijkheid, zoals een organisatie die niet is ingeschreven in het Handelsregister, een organisatie-onderdeel of een voorziening. Het nummer van een organisatie die voorkomt in een aangesloten register wordt ook beschouwd als een SubOIN.

> **Waarom hebben wij gekozen voor betekenisloze SubOIN's?** 
> In de discussie met betrokkenen is besproken op welke manier SubOIN's worden vastgelegd. Er zijn twee alternatieven besproken: 
> 1. Als basis het OIN van de rechtspersoon met een volgnummer van 3 cijfers in het suffix|
> 2. Een uniek betekenisloos nummer
> 
> Wij hebben gekozen voor een betekenisloos nummer vanwege een aantal redenen:
> Gebruikmaken van een suffix heeft een beperking tot 999 volgnummers. Dit lijkt een voldoende groot aantal maar vanwege de regel dat eenmaal ingetrokken SubOIN's nooit hergebruikt mogen worden is het bereiken van deze limiet niet ondenkbaar
> 
> Het is niet onmogelijk dat organisatieonderdelen wijzigen van een juridische verantwoordelijke, of dat een samenwerkingsverband van samenstelling wijzigt. Met een volgnummerconstructie wordt de ontkoppeling van rechtspersoon en SubOIN-houder onmogelijk.

Het prefix verwijst naar het SubOIN-register.

| **Element** | **Lengte** | **Waarde** |
|-----------------|------------|--------------------|
| **Prefix**| 8 posities | 00000004 |
| **Hoofdnummer** | 9 posities | Gegenereerd nummer |
| **Suffix**| 3 posities | 000|

Prefix tabel
------------

Een aangesloten overheidsregister krijgt een prefix (per uniek nummer) als het register wordt toegevoegd aan het OIN-stelsel. Dit wordt ook een SubOIN register genoemd. De prefix tabel wordt als aparte lijst beheerd door de Beheerder van het OIN-stelsel en wordt gepubliceerd op de website.

| **Prefix** | **Identificerend nummer** | **Bron**|
|------------|-----------------------------------------|---|
| 00000001 | RSIN| Handelsregister |
| 00000002 | Fi-nummer | Het fiscaal nummer wordt verstrekt door de Belastingdienst aan de organisatie zelf Het Fi-nummer kan worden gebruikt in het het geval voor onderdelen van de Staat der Nederlanden die niet ingeschreven in het Handelsregister zoals de Tweede Kamer der Staten-Generaal of de Algemene Rekenkamer. Het FI-nummer wordt verstrekt door de organisatie zelf |
| 00000003 | KvK nummer| Handelsregister Het KvK nummer wordt gebruikt door private partijen in de communicatie met de overheid. |
| 00000004 | subnummer | SubOIN register |
| 00000005 | Onderdelen van de Staat der Nederlanden | nog aan te wijzen |
| 00000006 | Onderdelen van het Rijk | nog aan te wijzen |
| 00000007 | BRIN nummer | De Basisregistratie Instellingen (BRIN) is een register van onderwijsinstellingen dat door DUO wordt beheerd in opdracht van het Ministerie van OCW.|
| 00000008 | Buitenlandse nummers| Op verzoek van een SubOINbeheerder door Logius uitgegeven nummers voor buitenlandse organisaties die niet in het Handelsregister zijn ingeschreven|
| 00000009 | UZI-nummer| Het Unieke Zorgverlener Identificatie Register (UZI-register) is de organisatie die de unieke identificatie van zorgaanbieders en indicatieorganen in het elektronisch verkeer mogelijk maakt.|
| 00000099 | Test OIN's| Elke organisatie mag een test OIN gebruiken mits voorzien van deze prefix.|

# Technologie-architectuur

** **


Schets van de COR
-----------------

Onderstaande plaat beschrijft de functionaliteiten van de COR op hoofdlijnen

![](media/27ee0a1c417f72dea1bdeb909a5ae35e.png)

Beschrijving van de onderdelen van COR

| **#** |**beschrijving rol of taak**|
|---|--------|
| 1| **Iedereen** Iedereen kan het publieke deel van de COR via een website benaderen.|
| 2| **Systeem toegang** De COR biedt een Restful API aan waarmee systemen het publieke deel van de COR automatisch kunnen bevragen |
| 3| **Logius Beheerder** De Logius beheerder kan na authenticatie conform de Logius richtlijnen in het besloten gedeelte van de COR OIN en SubOIN registrarties aanmaken, wijzigen of intrekken. |
||**Centrale OIN Raadpleegvoorziening**|
| 6| **OIN Raadpleegportaal** Webportaal. Op basis van een in te geven zoekitem (zoals deel van een naam van een organisatie of een OIN kan de OIN van een organisatie, de naam en de status (actief of ingetrokken) worden opgevraagd. Als er sprake is van een HoofdOIN – SubOIN relatie wordt deze getoond. De COR biedt ook de mogelijkheid om een CSV export te maken van de gehele registratie. |
| 8| **OIN-SubOIN Beheerportaal** Beheerders maken gebruik van het portaal om registraties aan te maken, te wijzigen of in te trekken.|
| 7| **Centrale OIN Raadpleegvoorziening Module** |
| 7A | **OIN Raadpleegapplicatie** De applicatie handelt de verzoeken van het OIN Raadpleegvoorziening portaal en de OIN Raadpleegservice af. De applicatie bevraagt het OIN register en retourneert zoekresultaten.|
| 7B | **OIN-Beheerapplicatie** De applicatie handelt de acties van het OIN- registratieportaal af. De applicatie registreert organisaties en organisatieonderdelen in het OIN-register . |
| 8| **Controleren of rechtspersoon bestaat** Bij het aanmaken van een registratie in het OIN register worden de gegevens van een geregistreerde Rechtspersoon online gecontroleerd in het Handelsregister. Daarnaast worden periodiek alle organisaties met een KvK nummer of RSIN gevalideerd. Indien een Rechtspersoon is opgeheven in het Handelsregister wordt de OIN registratie (en eventueel hieraan gekoppelde SubOINs) ingetrokken, |
||**Primaire Registers**|
| 9| **OIn en SubOIN-register** Het OIN en SubOIN worden in één register vastgelegd |
| 10 | **Handelsregister** Het Handelsregister is de primaire bron voor de COR. |
|| **Identificerende bronnen** Sommige overheidsorganisaties kennen naast registratie in het Handelsregisters en het OIN register ook andere identificerende nummers. Deze nummers worden aan een OIN registratie in het OIN register toegevoegd, en zijn via de CORAPI op te vragen. |
||De Ids uit deze bronnen op dit moment handmatig bijgewerkt in het OIN register bijgewerkt. |
| 11 | **RvIG** Gemeentecodes (BG codes)|
| 12 | **CBS** Provinciecodes en Waterschapcodes|
| 13 | **KOOP** Ministeriecodes |

# Bijlage A Begrippen

|begrip|omschrijving|
|---|---|
|**Centrale OIN Raadpleegvoorziening (COR)**|De COR biedt een publiek deel voor online inzage in de identificerende nummers van organisaties en organisatieonderdelen en biedt een besloten omgeving met een beheermodule voor het registreren van subOIN's. Het subOIN-register is onderdeel van de COR.|
|**TSP**|Certificatiedienstverlener (*Trust Service Provider*), marktpartijen die PKIoverheid certificaten verstrekken conform het Programma van Eisen van PKIoverheid. Voorheen CSP - Certificate Service provider-  genoemd.|
|**Digitaal berichtenverkeer**|het uitwisselen van gegevens via digitale berichten|
|**Erkend authenticatiemiddel**|Een authenticatiestelsel voor organisaties waarbij natuurlijke personen namens de organisatie worden gemachtigd om specifieke activiteiten te verrichten. Bijvoorbeeld eHerkenning, Idensys.|
|**Handelsregister (HR)**|Het Handelsregister is een bij wet ingestelde basisregistratie voor rechtspersonen en ondernemingen in Nederland. Het maakt deel uit van het stelsel van basisregistraties. Daarmee draagt het Handelsregister bij aan een efficiëntere overheid en aan een betere dienstverlening voor ondernemers. Zie <http://www.digitaleoverheid.nl>
|**KvK Nummer**|Het KvK nummer is het inschrijvingsnummer van de onderneming in het Handelsregister. Elke onderneming of maatschappelijke activiteit krijgt in het handelsregister één KvK-nummer, dit KvK-nummer bestaat altijd uit 8 cijfers. Bij bedrijfsoverdracht houden ondernemingen wijzigt hun KvK-nummer.|
|**Niet-natuurlijk persoon**|Een niet-natuurlijk persoon is een organisatie of samenwerkingsverband dat rechten en plichten heeft en wordt gedefinieerd aan de hand van het RSIN (bron KvK).|
|**OIN-beheerder**|Een overheidsorganisatie die is toegelaten om OIN of subOIN's aan organisaties toe te kennen. De OIN-beheerder draagt zorg voor de registratie van subOIN's voor organisaties die niet in een aangesloten register voorkomen maar die wel bij een broninstantie of op basis van brondocumenten kunnen worden geïdentificeerd en geverifieerd. De OIN-beheerder stelt de identificatie van een partij vast aan de hand van bewijsstukken of zelfstandig onderzoek.|
|**OIN-houder**|De OIN-houder is een rechtspersoon met een publieke taak, die gebruik maakt van het OIN. Alleen OIN houders met rechtspersoonlijkheid kunnen een subOIN aanvragen voor een organisatie of organisatieonderdeel die onder zijn juridische verantwoordelijkheid valt. Zij zijn verantwoordelijk voor de door hun aangevraagde subOIN(s).|
|**subOIN**|Organisaties en organisatieonderdelen die niet in een aangesloten overheidsregister voorkomen, komen mogelijk in aanmerking voor een subOIN. Deze worden geregistreerd in het subOIN-register. In eerdere publicaties over het OIN-beleid werd ook de term *OIN subnummer* gebruikt.|
|**subOIN-register**|Een register met alle uitgegeven OIN's die niet in een bronregister voorkomen.|
|**Organisatie**|Art 3.1 van *de NEN-ISO/IEC 6532-1* definieert een organisatie als een samenwerking van meerdere personen die met autoriteit acteren of mogen acteren ten behoeve van een doel *"a unique framework of authority within which a person or persons act, or are designated to act, towards some purpose''.*. Een organisatie kan een rechtspersoon zijn, of een samenwerking zonder rechtspersoonlijkheid die met autoriteit zelfstandig kan handelen.|
|**Organisatieonderdeel**|In de NEN – ISO/IEC 6532-1, Art.3.2 is de omschrijving van een organisatieonderdeel elke afdeling, dienst of entiteit binnen een organisatie die geïdentificeerd moet worden t.b.v. informatie-uitwisseling *"Any department, service or other entity within an* organization*, which needs to be identified for information interchange''*.| 
|**Overheidsregistraties**|Onder een overheidsregistratie wordt verstaan een landelijk dekkende registratie, met een wettelijke grondslag, waarin gegevens over individuele en identificeerbare objecten, subjecten of rechten zijn vastgelegd.|
|**PKIoverheid**|het Nederlandse stelsel van public key infrastructure dat door Logius wordt beheerd. Het Programma van Eisen (PvE) van PKIoverheid specificeert de eisen die aan de uitgifte van PKIoverheid certificaten door CSP's worden gesteld.|
|**Prefix**|de eerste 8 posities van het OIN komen overeen met een unieke code voor een uniek identificerend nummer uit een bronregister.|
|**Prefix tabel**|mapping tussen een unieke code en het identificerende nummer uit een bronregister (b.v. het RSIN nummer).|
|**RSIN**|Alle rechtspersonen en samenwerkingsverbanden, zoals bv's, verenigingen, stichtingen, vof's en maatschappen (eenmanszaken niet) krijgen bij inschrijving bij de KvK naast een KvK-nummer ook een Rechtspersonen en Samenwerkingsverbanden Informatienummer (RSIN). Dit nummer wordt gebruikt om gegevens uit te wisselen met andere (overheids)organisaties, zoals de Belastingdienst (bron KvK). Het RSIN is identiek aan het fiscale nummer.|
|**Voorziening**|De implementatie / fysieke realisatie van een systeem waarmee informatie of diensten daadwerkelijk geleverd worden, voorbeelden van voorzieningen zijn de Basisregistraties, MijnOverheid en Digilevering.|
