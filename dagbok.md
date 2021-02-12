**13. September**
Vi ble enige om å arbeide sammen på hovedprosjektet.


**16. September**
Eskil la fram muligheten om at hans tidligere arbeidsplass Huddly muligens kunne vært interessert i å komme med et oppdrag.


**13. Oktober**
Vi gjennomførte et møtet med Huddly, hvor vi kort ble litt kjent og de framla tre forslag for mulig prosjekter.


**20. Oktober**
Vi møttes for å diskutere litt og ble i all hovedsak enige at den beste kandidaten av de tre forslagene var gestur gjenkjenning. Her skrev vi også og leverte inn statusrapporten.


**27. Oktober**
Vi gjennomførte enda et møte med Huddly, hvor de la fram en beskrivelse av prosjektet vi valgte - gestur gjenkjenning. Vi snakket også kort om tekniske krav til feks. programmeringsspråk og eventuelle verktøy vi må ta i bruk.

**10. November**
Vi mottok ytterlig infromasjon samt en del tekniske krav til prosjektet, dette ble ført inn i prosjektskissen og levert inn.

**6. Januar**
Vi kontaktet interne og eksterne veiledere for å få til videomøter. Videre utforsket vi open-source-løsninger på lignende problem, samt potensielle platformer til utvikling og maskinlæring.

**7. Januar**
Videomøte med intern veileder Jianhua Zhang. Vi gikk gjennom hva som forventes av en bacheloroppgave og generelle tips til problemet vi prøvde å løse. En mer presis problemstilling ble etterlyst for forrapporten.

**8. Januar**
Inntil vi får satt et møte med Huddly bruker vi tid på å utforske allerede eksisterende løsninger. På dette punktet så mediapipe ut som et interessant alternativ.

**12. Januar**
Hadde et møte med veiledere, både intern og eksterne. Vi diskuterte litt rundt rammene for prosjektet, samt så litt på det vi hadde fått til så langt ved bruk av googles mediapipe bibliotek. Et nytt møte ble planlagt der vi skulle gå gjennom mer i detalj workflow, tilgjengelige ressurser, og lignende.

**22. Januar**
Denne uken hadde vi et møte med Huddly hvor vi sammen fikk planlagt rammene og målene for prosjektet i mer detalj. Det ble tydelig at vi hadde misforstått oppgaven litt og fokusert vel mye på bruken av maskinlæring i praksis. Det var tydelig at Huddly ønsket at vi i større grad skulle utvikle en modell på egenhånd, og dokumentere denne prosessen. Alt i alt var møtet givende og vi fikk finalisert alt vi trengte for forprosjektrapport og NDAer. Vi fikk også tips til hvordan vi skulle komme i gang med arbeidet: Første mål var å lage en maskinlæringsmodell som kunne detektere hender (object detection).

**26. Januar**
Analysert datasettet med hender for å prøve å utvikle en optimal strategi for å dele opp et bilde i mindre subbilder. Hvor vært subbilde enten inneholder eller ikke inneholder en hånd. Målet med dette er å sende hvert subbilde til en klassifiseringsmodell, for å oppnå en form for rudimentær lokalisering.

**28. Januar**
Eskil: Har sett på Tensorflow sitt object detect API, og prøvd å få trent modeller derifra ved hjelp av google cloud services. Hoveddelen av arbeidet har gått på å sette seg inn i tensorflow APIet, config filer og andre ting man må passe på. \
Jonathan: Har satt opp en enkel binær klassifiserings modell i keras, som tar inn et bilde og returnerer en skalar som beskriver sannsynligheten for at bildene inneholder en hånd. Bearbeidet egohands datasettet å brukte dette til å trene modellen. Sett noe på å koble denne modellen sammen med metoden for inndeling av bilder.

**5. Februar**
Torsdag denne uken hadde vi et møte med alle veiledere. Der fikk vi en ny og mer detaljert kravspesifikasjon. Kontrært til tidligere beskjeder, var det nå et ønske  om at vi fokuserte hovedsakelig på demonstrasjonen. Vi ble enige om å forsøke å levere en minimal versjon av produktet så snart som mulig, og  å i denne  benytte ferdige maskinlæringsløsninger for gestur-gjenkjenning. Eventuelle egne modeller kan tenkes å eventuelt bli implementert senere. Dette innebærer at en stor del av arbeidet vi har gjort opop til nå med å bygge opp og trene modeller blir lagt på is foreløpig, men læringsutbyttet fra denne prosessen vil nok uansett være av verdi.

**8. Februar**
Helgen og starten av uken var hovedsakelig dedikert til oppsettet av en generell struktur for mvpen etter kravspesifikasjonen. Her forsøkte vi å dele opp programmet logisk i mindre moduler, slik at hvert enkelt modul lett kan arbeides på og/eller byttes ut i ettertid. Vi startet med å implemetere mediapipe modellen og en simpel geometrisk gjenkjenning av gesturer som et modul i denne strukturen.

**11. Februar**
Et møte med veiledere ble holdt hvor fikk en liten introduksjon til å konfigurere huddlys kameraer og tilbakemeldinger på strukturen. Under dette møte fikk vi også en pekepinn for videre fremgang, hvor vi fikk fortalt at hovedfokus i ummidelbar framtig burde sentrere seg rundt å implementere en robust sjekk for om en gestur blir holdt og lage noe funksjonalitet som skal bli kontrollert av dette. Programmet ble også videreutviklet for å enkelt støtte både bilde- og videofiler i tillegg til webkamera.
