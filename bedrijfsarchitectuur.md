# Bedrijfsarchitectuur

![Logo\_vZVZ\_servicecentrum.JPG](.gitbook/assets/0%20%281%29.jpeg)



## Doel en aanleiding

### Doel en scope

Dit document beschrijft de bedrijfsarchitectuur van Koppeltaal GGZ versie 1.3.x. Dit document is opgesteld onder verantwoording van VZVZ. De scope is een beschrijving van de architectuur op ‘Enterprise Architectuur’ niveau, waarbij het TOGAF-raamwerk, en de Architectuur Development Methode \(ADM\) zoveel mogelijk gebruikt worden als taal voor vastlegging van de architectuur.

### Leeswijzer

Dit architectuurdocument is bedoeld voor VZVZ om vragen te kunnen beantwoorden over huidige mogelijkheden en beperkingen van Koppeltaal en dient als basis voor eventuele uitbreiding van functionaliteiten. Het document bevat eveneens \(verwijzingen naar\) standaarden die door GGZ-instellingen en ICT-leveranciers voor die instellingen voor behandelprocessen en de daarbij behorende gegevensuitwisseling.

De architectuurbeschrijving is onder te verdelen in drie secties, namelijk de ‘Bedrijfsarchitectuur’, de ‘Informatiesystemen architectuur’ en de ‘Technologie architectuur’.

![Koppeltaal architectuur](.gitbook/assets/1%20%281%29.jpeg)

### Eenheid van taal

De architectuur van Koppeltaal GGZ heeft zich over de afgelopen vier jaar ontwikkeld op basis van de visie op architectuur die aan de start van het project in 2014 ontwikkeld is. Gedurende die vier jaar is er veel gebeurd en zijn er steeds meer GGZ-aanbieders aangesloten binnen de complexe en multidisciplinaire ‘sector’ die de GGZ is. Gedurende dezelfde periode heeft de informatie-uitwisseling in de zorg een grote ontwikkeling doorgemaakt. Voorbeelden zijn het programma MedMij, de nieuwe GGZ, Positieve gezondheid, het informatieberaad, en de wereldwijde adoptie van FHIR. De invloed van deze ontwikkelingen, en veranderingen hebben geleid tot een diversiteit van gebruik van begrippen binnen Koppeltaal.

### Kaders en uitganspunten

#### Normatief

De onderstaande documenten zijn normatieve standaarden voor dit document.

#### Informatief

De onderstaande documenten zijn ter ondersteuning bij specifieke onderwerpen in dit document.

| Referentie | Document | Versie |
| :--- | :--- | :--- |
| \[NEN7510\] | NEN 7510 ‘Medische informatica - Informatiebeveiliging in de zorg’ is een Nederlandse norm die maatregelen beschrijft die zorginstellingen moeten nemen om op adequate wijze met patiëntgegevens om te gaan. |  |
| \[ISO-norm 25010\] | ISO-norm 250101 beschrijft kwaliteitskenmerken van software. |  |

## Koppeltaal

### Geestelijke zorgverlening, blended care en behandelplan

Koppeltaal integreert informatiestromen uit eHealth-modules, ROM en EPD in de werkomgeving van de behandelaar en cliënt. Zo heeft de behandelaar direct een volledig en actueel beeld van hun cliënt in één omgeving. Daarnaast is het mogelijk voor behandelaren om hun cliënten toegang te geven tot specifieke eHealth-modules en interventies van uiteenlopende leveranciers.

Interoperabiliteit tussen de informatiesystemen is hier één van de belangrijke aspecten in de context van **blended care in de GGZ**. Bij blended care in de GGZ worden reguliere face-to-face gesprekken gecombineerd met **online interventies** zoals bijvoorbeeld chat, beeldbellen en **online behandelmodules**. Hierdoor kan een cliënt tijd- en plaats-onafhankelijk zorg gebruiken via een tablet of smartphone.

Een **behandelplan** beschrijft de gehele behandeling waar een blended care behandeling onderdeel van kan zijn. In dat plan worden verschillende **activiteiten** benoemd, veelal in een bepaalde volgorde. Deze activiteiten kunnen zijn, het samenstellen van het zorgteam, het bepalen van de doelen van een behandeling, het maken van een afspraak, het uitvoeren van een \(online\) interventie, het bespreken of bekijken van **voortgang**, **status**, **resultaten**, en het **evalueren** van de vooruitgang van de conditie van de Cliënt ten opzichte van de behandeldoelen. Voor zover deze activiteiten door een informatiesysteem worden ondersteund, is gegevensuitwisseling via Koppeltaal mogelijk.

Bij een blended care behandeling zijn tenminste een **cliënt** en een **behandelaar** betrokken. En steeds vaker ook **derden**, zoals vrienden, familie, lotgenoten, en ervaringsdeskundigen.

### Positie van Koppeltaal in het GGZ-referentiedomeinen model

![Koppeltaal en het GGZ-referentiedomein model](.gitbook/assets/2%20%282%29.jpeg)

In het door GGZ Nederland en Nictiz opgestelde GGZ Domein referentiemodel speelt Koppeltaal een mogelijke rol in de met een groene cirkel aangeduide sub domeinen.

Koppeltaal helpt om behandeling te ondersteunen. Specifiek eHealth in blended care processen. Verder ondersteunt Koppeltaal de aanmeldingsprocessen via het synchroniseren van patiëntgegevens over verschillende applicaties. Daarnaast kan Koppeltaal \[in de toekomst\] een rol spelen in de resourceplanning, omdat er rond een behandelplan met Koppeltaal relaties gelegd kunnen worden tussen cliënt, behandelaar, en derden \(zoals familie, vrienden, ervaringsdeskundigen, etc.\).

Ten slotte kan Koppeltaal \[in de toekomst\] een rol spelen in de verantwoording en de innovatie. Via Koppeltaal kan informatie voor besturing verkregen worden over de inzet van eHealth in blended care processen geïntegreerd over verschillende applicaties heen. Daarnaast kan met Koppeltaal, de adoptie van eHealth onder cliënten en behandelaren versneld worden via de door Koppeltaal veroorloofde keuzevrijheid, flexibiliteit, en gebruikersgemak.

### Juridische kader

In de context van Koppeltaal spelen de volgende juridische concepten, relaties, en regels een rol:

* Behandelrelatie
* Contractuele relaties
* Gebruik van burgerservicenummer in de zorg
* AVG-normen

Behandelrelatie. Een behandelrelatie in het kader van de WGBO wordt aangegaan door de GGZ-deelnemers van Koppeltaal. De verantwoordelijkheid voor de gegevensverwerking in de context van deze overeenkomst ligt bij de GGZ-deelnemers.

De GGZ-deelnemers van Koppeltaal hebben contractuele relaties met ICT-leveranciers die voor hen gegevens verwerken. Deze relatie wordt tevens via een verwerkersovereenkomst geregeld.

GGZ Gebruikers vragen hun IT-leveranciers gegevens uit te wisselen via Koppeltaal in de context van de behandelrelatie. IT-leveranciers worden hiervoor deelnemer in Koppeltaal en accepteren daartoe de IT-deelnemersvoorwaarden. Tevens sluiten ze met Koppeltaal een verwerkersovereenkomst.

Indien gebruik wordt gemaakt van het BSN bij gegevensuitwisseling, geldt ook de wet gebruik Burgerservicenummer in de zorg \(Wgbsn-z\). De wet gebruik Burgerservicenummer in de zorg verplicht zorgaanbieders het Burgerservicenummer \(BSN\) van hun patiënten vast te leggen in hun administratie. Met het BSN kan de identiteit van de patiënt zeker worden gesteld. In het geval een persoon \(patiënt\) zich voor het eerst tot een zorgverlener wendt, moet de zorgverlener bij het eerste fysieke contact het BSN verifiëren. Vervolgens valt de interactie tussen de persoon en zijn zorgverlener onder het vervolg van de verlening van zorg. Voor dit vervolg van de verlening van zorg mag het BSN worden verwerkt. IT-leveranciers kunnen het BSN opslaan onder de verantwoordelijkheid van de GGZ-deelnemers \(in het bijzonder EPD-leveranciers\), en gebruiken vervolgens een pseudoniem \(EPD-nummer\) bij gegevensuitwisseling via Koppeltaal ter referentie.

Via het privacy beleid van de GGZ-deelnemer, en de keten van verwerkersovereenkomsten zoals hierboven beschreven \(en de maatregelen die ten gevolge van die overeenkomsten in de deelnemende organisaties en de Koppeltaal keten worden ingevoerd\) voldoet Koppeltaal aan de AVG-normen.

## Scenario’s, rollen en use-cases

### Scenario’s

Koppeltaal biedt via de standaard: flexibiliteit, keuzevrijheid en gebruiksgemak in blended care processen. Om te illustreren hoe de standaard dat doet beschrijven we hieronder twee voorbeeld scenario’s van verschillende blended care behandelingen. Een in de eerstelijns zorg en een in de gespecialiseerde GGZ zorg. De stappen in de scenario’s staan in de linker kolom beschreven, en in de rechterkolom staan Koppeltaal use cases die gebruikt worden in de ondersteuning van de betreffende stap in het proces.

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Scenario</b>
      </th>
      <th style="text-align:left"><b>Scenario per stap</b>
      </th>
      <th style="text-align:left"><b>Use case</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">Een cli&#xEB;nt meldt zich bij de huisarts met chronische spanning en
        hoofdpijn. De huisarts constateert dat er veel angst speelt bij deze cli&#xEB;nt
        en vraagt de praktijkondersteuner GGZ (POH) de cli&#xEB;nt te begeleiden.
        De POH opent de pagina van deze cli&#xEB;nt en kijkt in de lijst met beschikbare
        applicaties welke angstmodule de cli&#xEB;nt het best kan volgen. Ze ziet
        een geschikte module angst en spanning.</td>
      <td style="text-align:left">
        <ul>
          <li>Beheerder heeft applicaties met daarbij behorende (sub)activiteiten in
            het Koppeltaal domein geregistreerd en daarmee zijn ze beschikbaar gesteld</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">Ze wijst deze module toe aan de cli&#xEB;nt.</td>
      <td style="text-align:left">
        <ul>
          <li>Behandelplan starten
            <ol>
              <li>(Sub)activiteiten als onderdeel van het behandelplan selecteren.</li>
              <li>Participant (Pati&#xEB;nt) opvoeren in het behandelplan.</li>
            </ol>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">De cli&#xEB;nt ontvangt in de mail een uitnodiging voor toegang tot het
        cli&#xEB;ntportaal van de huisarts en logt in via een link.</td>
      <td style="text-align:left">
        <ul>
          <li>Ontvangen inlogverzoek</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">In het cli&#xEB;ntportaal staat de module angst en spanning als een &#x2018;blok&#x2019;
        klaar zoals besproken. De cli&#xEB;nt klikt op het blok en de module wordt
        geopend. De cli&#xEB;nt gaat aan de slag. De cli&#xEB;nt werkt een half
        uur aan de module en sluit deze na afronding af en gaat slapen.</td>
      <td
      style="text-align:left">
        <ul>
          <li>(Sub)activiteit lanceren
            <ol>
              <li>Single Sign-On realiseren tussen interventie en de te lanceren (sub)activiteit.</li>
            </ol>
          </li>
        </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">De POH komt in de ochtend op kantoor en opent het cli&#xEB;nt dossier
        via het behandelaarsplatform. Ze ziet dat de cli&#xEB;nt de module heeft
        geopend, heeft afgerond en vervolgens heeft afgesloten.</td>
      <td style="text-align:left">
        <ul>
          <li>(Sub)activiteit monitoren.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Ze klikt door naar de pagina van de cli&#xEB;nt en kan daar direct de
        scores van de app en de reflectie van de cli&#xEB;nt daarop lezen.</td>
      <td
      style="text-align:left">
        <ul>
          <li>(Sub)activiteit evalueren.</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">Ze twijfelt of ze de reflectie van de cli&#xEB;nt op de afsluitende opdracht
        van de module goed begrijpt. Ze klikt door op het resultaat, daarmee wordt
        de module geopend en kan ze zien wat de cli&#xEB;nt precies gedaan heeft
        in de opdracht. Nu is ze goed voorbereid voor het gesprek van vanmiddag.</td>
      <td
      style="text-align:left">
        <ul>
          <li>(Sub)activiteit evalueren door (sub)activiteit te lanceren.</li>
        </ul>
        </td>
    </tr>
  </tbody>
</table>

Tabel 1. Eerstelijns zorg scenario – Use-cases

In de specialistische GGZ zou Koppeltaal bijvoorbeeld in het volgende scenario ingezet kunnen worden:

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Scenario</b>
      </th>
      <th style="text-align:left"><b>Scenario per stap</b>
      </th>
      <th style="text-align:left"><b>Use case</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">Een cli&#xEB;nt is in gesprek met de psychiater. Er is complexe problematiek
        aan de orde, maar de problematiek is niet ernstig. Er kan behandeld worden
        met blended care. De psychiater kiest een passende ROM-vragenlijst om beter
        beeld te krijgen van de startsituatie van de behandeling.</td>
      <td style="text-align:left">
        <ul>
          <li>Selecteer passende ROM-vragenlijst (sub activiteit) aan cli&#xEB;nt.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">De cli&#xEB;nt ontvangt via de e-mail een uitnodiging om in te loggen</td>
      <td
      style="text-align:left">
        <ul>
          <li>Ontvangen inlogverzoek.</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">De cli&#xEB;nt logt in en ziet een knop om de vragenlijst te starten.
        De cli&#xEB;nt klikt en de vragenlijst wordt geopend. De cli&#xEB;nt vult
        de lijst in, maar stopt halverwege. Te moeilijk.</td>
      <td style="text-align:left">
        <ul>
          <li>Opstarten en (gedeeltelijk) invullen ROM vragenlijst (sub activiteit)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">De behandelaar krijgt melding dat cli&#xEB;nt geen voortgang toont in
        behandeling</td>
      <td style="text-align:left">
        <ul>
          <li>(Sub)activiteit monitoren.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left">De cli&#xEB;nt geeft aan dat hij de vragenlijst moeilijk vindt en dat
        hij daarop afhaakt. Dat is onderdeel van het probleem waarom de cli&#xEB;nt
        in de eerste plaats kwam. In overleg besluiten behandelaar en cli&#xEB;nt
        een familielid bij te schakelen om te helpen. Het familielid kan dat op
        zijn eigen systeem zien wat de cli&#xEB;nt heeft ingevuld en daarop toelichting
        geven voor de behandelaar. De cli&#xEB;nt nodigt via het eHealthplatform
        zijn vrouw uit om mee te helpen.</td>
      <td style="text-align:left">
        <ul>
          <li>Participant (Derde) opvoeren in het behandelplan.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left">De behandelaar krijgt een signaal dat er een relatie is toegevoegd aan
        de pagina van de cli&#xEB;nt.</td>
      <td style="text-align:left">- Ontvangen signaal dat relatie is toegevoegd</td>
    </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left">Met behulp van zijn vrouw lukt het de client om de vragenlijst af te ronden.
        De behandelaar krijgt signaal van de afronding en bekijkt de resultaten
        ter voorbereiding op het volgende gesprek.</td>
      <td style="text-align:left">
        <ul>
          <li>(Sub)activiteit evalueren</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">15</td>
      <td style="text-align:left">In gesprek besluiten cli&#xEB;nt en behandelaar voor maatwerk op het gebied
        van eHealth en monitoring. De cli&#xEB;nt gaat een app gebruiken om zelf
        doelen te stellen, te monitoren en met zijn familie en vrienden passende
        content voor zelfzorg te verzamelen. De behandelaar kent de betreffende
        app toe aan de cli&#xEB;nt.</td>
      <td style="text-align:left">
        <ul>
          <li>Behandelplan starten
            <ol>
              <li>(Sub)activiteiten als onderdeel van het behandelplan selecteren.</li>
            </ol>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">16</td>
      <td style="text-align:left">De cli&#xEB;nt logt thuis in en ziet een code om de app te activeren en
        instructies om de app via de appstore te installeren op zijn iPhone. Hij
        gebruikt de code om de app te activeren. (De app voor die gebruiker wordt
        aangemeld voor berichten van Koppeltaal)</td>
      <td style="text-align:left">
        <ul>
          <li>(Sub)activiteit lanceren
            <ol>
              <li>(met SSO)</li>
            </ol>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">17</td>
      <td style="text-align:left">De behandelaar ziet met regelmaat status, voortgang en resultaten uit
        de app van de cli&#xEB;nt.</td>
      <td style="text-align:left">
        <ul>
          <li>(Sub)activiteit monitoren.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">18</td>
      <td style="text-align:left">Op een gegeven moment denkt de behandelaar aan een filmpje op internet
        waarvan hij denkt dat het behulpzaam kan zijn voor in de &#x2018;rugzak&#x2019;
        van deze cli&#xEB;nt. Hij kopieert een link naar het filmpje in een bericht
        dat hij de cli&#xEB;nt stuurt. De cli&#xEB;nt opent de app in de ochtend
        en ziet daar een tip van zijn behandelaar. De cli&#xEB;nt bekijkt de tip
        en voegt deze toe aan zijn &#x2018;rugzak&#x2019; in de app.</td>
      <td style="text-align:left">
        <ul>
          <li>Algemene informatie uitwisselen</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

Specialistische zorg scenario – Use-cases

Koppeltaal biedt de volgende rollen en use-cases aan om de scenario’s, zoals hierboven beschreven, mogelijk te maken.

![Use-cases](.gitbook/assets/3%20%282%29.jpeg)

### Rollen

* Beheerder. Degene die de applicaties\(interventies\) activeert en activiteiten beschikbaar stelt ten behoeve van een zorginstelling en zorgverleners.
* Patiënt. Degene die behandeld wordt.
* Behandelaar. Degene die de zorg aan de patiënt verleent.
* Derde. Degene die een niet zorg verlenende relatie hebben met de patiënt en ondersteuning biedt bij een behandeling, zoals vrienden, familie, lotgenoten, en ervaringsdeskundigen.

### Use-cases

#### Applicatie registreren

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-01</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">Applicatie registreren</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 1</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Applicatie per zorgbehoefte geregistreerd in het Koppeltaal domein</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Beheerder</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Applicatie (interventie)</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left">Applicatie moet gecertificeerd zijn</td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Beheerder is trigger en doet configuratie van zorgdomein</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left">(Interventie) applicatie actief in zorgdomein</td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### \(Sub\)activiteiten registreren

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-02</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">(Sub)activiteiten registreren</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 1</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Per applicatie worden activiteiten definities geregistreerd, die aangeboden
        worden op basis van aandoening en behoeften van de cli&#xEB;nt.</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Beheerder</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Activiteiten definitie</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left">Applicatie actief in zorgdomein</td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Beheerder is trigger</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left">(Sub)activiteiten beschikbaar</td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### Behandelplan opzetten

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-03</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">Behandelplan opzetten</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 2</li>
          <li>Scenario 8</li>
          <li>Scenario 12</li>
          <li>Scenario 15</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Het opzetten en/of aanpassen van een behandelplan door het kiezen van
        activiteiten en participanten op basis van aandoening en behoefte client</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Behandelaar/Behandelteam</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Behandelplan</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left">Behandelaar en Pati&#xEB;nt zijn bekend. Activiteiten zijn beschikbaar</td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Behandelaar stelt met Pati&#xEB;nt een behandelplan samen.</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left">Behandelplan aanwezig en behandelrelatie gelegd tussen Behandelaar en
        Pati&#xEB;nt</td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left">Behoefte van pati&#xEB;nt staat voorop</td>
    </tr>
  </tbody>
</table>

#### \(Sub\)activiteiten selecteren

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-04</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">(Sub)activiteiten selecteren</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 2.1</li>
          <li>Scenario 8</li>
          <li>Scenario 15</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Het selecteren van (sub)activiteiten adhv definities op basis van aandoening
        en behoefte van cli&#xEB;nt</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Behandelaar</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Activiteit</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left">Activiteitenlijst van definities</td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Selecteren van activiteiten door behandelaar</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left">Activiteiten toegevoegd aan behandelplan</td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### \(Sub\)activiteit lanceren

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-05</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">(Sub)activiteit lanceren</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 4</li>
          <li>Scenario 7</li>
          <li>Scenario 10</li>
          <li>Scenario 16</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Het lanceren of opstarten van een activiteit</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Pati&#xEB;nt</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">(Sub)activiteit lanceren</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left">Activiteit geselecteerd</td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Nadat activiteit geselecteerd is, krijgt participant een link naar applicatie
        (interventie) om activiteit uit te voeren. Het linkje is de trigger.</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left">Activiteiten kunnen op verschillende manieren en locaties gestart en uitgevoerd
        worden. Hierbij is het Single Sign-On principe van groot belang. Eenmalige
        identificatie.</td>
    </tr>
  </tbody>
</table>

#### \(Sub\)activiteit monitoren

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-06</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">(Sub)activiteit monitoren</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 5</li>
          <li>Scenario 11</li>
          <li>Scenario 17</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Voortgang en status van activiteiten volgen, die door de pati&#xEB;nt
        wordt uitgevoerd</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Behandelaar</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Activiteiten status</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left">Activiteiten opgenomen in Behandelplan</td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Status wijziging van activiteit</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### \(Sub\)activiteit evalueren

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-07</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">(Sub)activiteit evalueren</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 6</li>
          <li>Scenario 7</li>
          <li>Scenario 14</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Aan het eind of tijdens een activiteit door een participant, een uitkomst
        of de tot dusver behaalde resultaten van bijvoorbeeld een voltooide sub-sectie
        ingevulde vragenlijst van een activiteit doorgegeven</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Behandelaar</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Activiteiten resultaat</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Pati&#xEB;nt trigger deze use case</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### Participant opvoeren

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-08</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">Participant opvoeren</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 2.2</li>
          <li>Scenario 12</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Bij behandelplan kunnen gebruikers of participanten: pati&#xEB;nt, behandelaar(s)
        en derden toegevoegd worden. Behandelaar wordt toegewezen aan een pati&#xEB;nt
        (behandelrelatie). Derden worden aan pati&#xEB;nt gerelateerd.</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Behandelaar en Behandelteam worden toegewezen aan Pati&#xEB;nt</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Behandelaar (Behandelteam), Pati&#xEB;nt en Derde</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Trigger is het behandelplan waar de relaties tussen participanten wordt
        vastgelegd</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### Inlogverzoek sturen naar participant

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-09</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">Inlogverzoek ontvangen</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 3</li>
          <li>Scenario 9</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Na behandelplan ingevoerd te hebben en behandelaar toegewezen is aan pati&#xEB;nt,
        krijgt pati&#xEB;nt inlogverzoek om met activiteiten te beginnen</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Participant</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Inlogverzoek</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left">Behandelplan activiteit</td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Behandelaar triggert de use case na selectie van activiteiten</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### Derden toegevoegd signalering

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-10</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">Derden toegevoegd signalering</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 13</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">In overleg met behandelaar besluiten derden bij te schakelen om te helpen.
        Zodra client, derden ingeschakeld heeft, wordt behandelaar hierover ge&#xEF;nformeerd.</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Pati&#xEB;nt</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Signalering naar Behandelaar</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">De pati&#xEB;nt is de trigger om behandelaar te informeren</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left">Derde opgevoerd</td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### Algemene informatie uitwisselen

<table>
  <thead>
    <tr>
      <th style="text-align:left">Use case</th>
      <th style="text-align:left">UC-KT-11</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Naam</td>
      <td style="text-align:left">Algemene informatie uitwisselen</td>
    </tr>
    <tr>
      <td style="text-align:left">Scenario</td>
      <td style="text-align:left">
        <ul>
          <li>Scenario 18</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Beschrijving</td>
      <td style="text-align:left">Eenvoudige ongestructureerde informatie uitwisselen tussen participanten</td>
    </tr>
    <tr>
      <td style="text-align:left">Primaire actor</td>
      <td style="text-align:left">Participanten (Behandelaar, Pati&#xEB;nt, Derde)</td>
    </tr>
    <tr>
      <td style="text-align:left">Onderwerp</td>
      <td style="text-align:left">Algemene informatie</td>
    </tr>
    <tr>
      <td style="text-align:left">Pre-condities</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Trigger</td>
      <td style="text-align:left">Participanten die algemene informatie willen delen met anderen, in de
        context van een behandeling</td>
    </tr>
    <tr>
      <td style="text-align:left">Procesflow</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Post-conditie</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Opmerkingen</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### Bedrijfsobjecten

De use-cases benoemen niet alleen de actoren, maar noemen ook “bedrijfsobjecten”, zoals Behandelplan, Activiteit, Behandelaar, Patiënt en Derde. Het volgende model toont de bedrijfsobjecten en hun onderliggende relaties.

![Bedrijfsobjecten](.gitbook/assets/4%20%282%29.jpeg)

### Beheerprocessen

Om Koppeltaal als integratie standaard van informatiesystemen ter beschikking te stellen voor instellingen voor Geestelijke Gezondheidszorg, zijn er beheerprocessen nodig tussen zorgaanbieders, leveranciers en stichting Koppeltaal.

We onderscheiden de volgende functionele beheer lagen \(zie Beheerprocessen\).

We hebben **Koppeltaalregie** die de kwaliteit en levering van uitbestede diensten door aanbieders coördineert.

We hebben **Koppeltaalketen** die ervoor zorgt dat de juiste gegevens en informatie beschikbaar komt voor de ketenpartners van Koppeltaal en het aanmeldpunt is van meldingen, verzoeken en gegevens.

We hebben **Koppeltaalcomponenten** die ervoor zorgt dat de verschillende Koppeltaal componenten \(systemen\) beschikbaar zijn voor de ondersteuning en gebruikersbeheer van informatievoorziening. Daarnaast wordt gekeken of de Koppeltaal componenten in lijn zijn met de gestelde bedrijfsdoelen. Deze worden vastgelegd in architectuurproducten en bewaakt door de architectuur.

We hebben **Koppeltaaldiensten** die onderverdeeld zijn in de volgende ondersteunende beheerprocessen:

* Functioneel beheer. Het in stand houden en aansturen van de informatievoorziening.
* Domeinbeheer. Het ervoor zorgen dat de domeinen beschikbaar zijn
* Identiteitenbeheer. Het beheren en beschikbaar stellen van gegevens van gebruikers en hun autorisaties.
* Applicatiebeheer. Het aanpassen van toepassingsprogrammatuur en gegevensverzamelingen.
* Infrastructuurbeheer Het in stand houden en beheren van de-infrastructuur en ontwikkelingen daarvan.
* Applicatieontwikkeling Het ontwikkelen toepassingsprogrammatuur en gegevensverzamelingen.

De rollen Regie- en Keten Support worden door VZVZ-servicecentrum uitgevoerd

De Leverancier Support rol worden door de verschillende ICT- en adapter leveranciers ingevuld. De Koppeltaal Support wordt in eerste instantie door VZVZ uitgevoerd.

![Beheerprocessen](.gitbook/assets/5%20%281%29.jpeg)

## Koppeltaal kwaliteitseisen \(ISO-norm 250101\)

Niet-functionele \(software\) requirements zijn kwaliteitseisen waaraan een systeem moet voldoen. De ISO-norm 25010 beschrijft de [kwaliteitskenmerken](https://nl.wikipedia.org/wiki/Kwaliteit_%28hoedanigheid%29) van [software](https://nl.wikipedia.org/wiki/Software). Het model voor productkwaliteit onderscheidt acht hoofdcategorieën.

1. **Functionele geschiktheid** \(Functional suitability\). De mate waarin een softwareproduct of computersysteem functies levert die voldoen aan de uitgesproken en veronderstelde behoeften, bij gebruik onder gespecificeerde condities.
2. **Prestatie-efficiëntie** \(Performance efficiency\). De prestaties in verhouding tot de hoeveelheid middelen gebruikt onder genoemde condities.
3. **Uitwisselbaarheid** \(Compatibility\). De mate waarin een product, systeem of component informatie uit kan wisselen met andere producten, systemen of componenten, en/of het de gewenste functies kan uitvoeren terwijl het dezelfde hard- of software-omgeving deelt.
4. **Bruikbaarheid** \(Usability\). De mate waarin een product of systeem gebruikt kan worden door gespecificeerde gebruikers om effectief, efficiënt en naar tevredenheid gespecificeerde doelen te bereiken in een gespecificeerde gebruikscontext.
5. **Betrouwbaarheid** \(Reliability\). De mate waarin een systeem, product of component gespecificeerde functies uitvoert onder gespecificeerde condities gedurende een gespecificeerde hoeveelheid tijd.
6. **Beveiligbaarheid** \(Security\). De mate waarin een product of systeem informatie en gegevens beschermt zodat personen, andere producten of systemen de juiste mate van gegevenstoegang hebben passend bij hun soort en niveau van autorisatie.
7. **Onderhoudbaarheid** \(Maintainability\). De mate waarin een product of systeem effectief en efficiënt gewijzigd kan worden door de aangewezen beheerders.
8. **Overdraagbaarheid** \(Portability\). De mate waarin een systeem, product of component effectief en efficiënt overgezet kan worden van één hardware, software of andere operationele of gebruiksomgeving naar een andere.

Voor de Koppeltaal kwaliteitseisen wordt gekeken naar de uitwisselbaarheid, bruikbaarheid, betrouwbaarheid, beveiligbaarheid en onderhoudbaarheid.

### Uitwisselbaarheid - koppelbaarheid \(interoperability\)

De mate waarin Koppeltaal informatie uit kan wisselen met andere eHealth producten of componenten, en/of het de gewenste functies kan uitvoeren. Dit vereist eenheid van taal tussen de eHealth producten of componenten. Hiervoor wordt HL7 FHIR als normatieve standaard gebruikt. De FHIR resources zijn in de basis generiek en worden met behulp van profielen uitgebreid en specifieker gemaakt voor een specifieke toepassing. Door de manier waarop profiling wordt toegepast, kunnen er voor een bepaalde basis resource een groot aantal verschillende profielen bestaan, afhankelijk van zorgdomein, instelling of leverancier. Om interoperabiliteit te borgen is het van belang dat binnen een bepaalde use case dezelfde profielen gebruikt worden. Hiervoor zullen dienstverleners onderling nadere afspraken moeten maken over de gebruikte profielen, onder de regie van Koppeltaal. Daarbij staat het doel van de informatie-uitwisseling centraal \(een optimale ondersteuning van de patiënt in zijn persoonlijke proces van herstel\) en worden er geen gegevens uitgewisseld zonder toestemming van de patiënt, behoudens informatie-uitwisseling tussen medebehandelaars omdat de toestemming van de patiënt dan wordt verondersteld te zijn gegeven. In de uitwisselbaarheid wordt ook aandacht besteed aan de uitwisseling van informatie met derden in relatie tot een patiënt.

### Bruikbaarheid \(usability\) - toegankelijkheid \(accessibility\)

De mate waarin aangeleverde interventies snel en eenvoudig gebruikt kunnen worden door participanten om effectief, efficiënt en naar tevredenheid gespecificeerde doelen te bereiken in een gespecificeerde gebruikscontext. Om interventies te kunnen lanceren en in te kunnen zetten voor verschillende toepassingen wordt gebruik gemaakt van Single Sign-On \(SSO\) bij het lanceren van interventies \(eHealth modules\). Hierbij worden participanten eenmalig geauthenticeerd waarna ze automatisch toegang krijgen tot meerdere applicaties en resources in een domein van Koppeltaal. In Koppeltaal 1.3.x wordt naast SSO ook gebruik gemaakt van SMART. SMART biedt een standaard voor de manier waarop eHealth platforms en modules worden geverifieerd en geïntegreerd. Door deze processen te standaardiseren, kunnen zorgverleners meer verschillende interventies gebruiken en kunnen ICT-leveranciers eHealth platformen voor een breder publiek ontwikkelen.

### Betrouwbaarheid \(reliability\) - beschikbaarheid \(availability\)

De mate waarin een eHealth module gespecificeerde functies uitvoert onder gespecificeerde condities gedurende een gespecificeerde hoeveelheid tijd.

Behandelaren willen eHealth modules \(interventies\) in kunnen zetten wanneer het gewenst is en moeten dus dan beschikbaar en toegankelijk zijn.

### Beveiligbaarheid \(security\)

De mate waarin informatie en gegevens \(resources\) beschermt moet worden zodat \(eind\)gebruikers, en andere producten de juiste mate van gegevenstoegang hebben passend bij hun soort en niveau van autorisatie. Naast het borgen van kwaliteitscriteria vereist de norm NEN 7510 dat informatiebeveiligingsmaatregelen op controleerbare wijze zijn ingericht voordat kan worden gesproken over adequate informatiebeveiliging.

* Vertrouwelijkheid \(Confidentiality\) De mate waarin een product of systeem ervoor zorgt dat gegevens alleen toegankelijk zijn voor diegenen die geautoriseerd zijn. Participanten mogen bijvoorbeeld alleen hun eigen behandelplan inzien.
* Integriteit \(Integrity\) De mate waarin een systeem, product of component ongeautoriseerde toegang tot of aanpassing van gegevens verhindert. Alleen geregistreerde interventies krijgen toegang tot een Koppeltaal domein en hebben invloed op de activiteitenstatus. Uitkomsten en/of behaalde resultaten van bijvoorbeeld ingevulde vragenlijsten van een doorgegeven activiteit, worden op hun juistheid en volledigheid gecontroleerd.
* Verantwoording \(Accountability\) De mate waarin acties van een entiteit getraceerd kunnen worden naar die specifieke entiteit. Koppeltaal genereert log-informatie voor allerlei activiteiten, zoals het registreren of aanpassen van een behandelplan, maar ook technische logs met storingen van systemen. De log-informatie van Koppeltaal stelt zorgaanbieders, toezichthouders en cliënten/patiënten in staat om handelingen te kunnen volgen en naderhand te kunnen controleren.

### Onderhoudbaarheid \(maintainability\)

De mate waarin Koppeltaal effectief en efficiënt gewijzigd kan worden door aangewezen beheerders \(zie ook paragraaf 3.5 Beheerprocessen\). Dit gaat over de configuratie en beheer van:

* domeinen
* applicaties \(modularity\)
* interacties \(functionaliteit\)
* beheerders \(identiteit\)
* toegangslog beheer \(systemen\)
