<details open>
<summary>Tirsdag <sub>25/03</sub></summary>
I dag har jeg planlagt datamodell og app layout. Jeg har skrevet plandokumentet og levert det inn. I tillegg har jeg lagt mesteparten av SQL Objektene og skrevet SQL Templates.
</details>
<details open>
<summary>Onsdag <sub>26/03</sub></summary>
I dag har jeg grovt lagt det meste av kjernefunksjonaliteten i alle tre appene. Et avvik fra planen skjedde i dag, der jeg endte opp med å måtte lage en modal for å legge til forfattere siden en skal kunne ha flere forfattere på en bok. Har også valgt å bytte ISBN til et NVARCHAR(17) felt for å støtte bindestrek i ISBN format xxx-xx-xxxxx-xx-x.
</details>
<details open>
<summary>Torsdag <sub>27/03</sub></summary>
I dag har jeg et par avvik: lagt til [Deleted] for soft delete i atbl_Library_Books, lagt til Manage Tags, Authors og Genre som ikke var planlagt.
Jeg fikk endringen fra fagprøvenemnden, som var "ingen endring", så da har jeg ferdigstillt det grove produktet og begynt å finpusse og legge til ekstrafunksjonalitet. Så langt i ekstra funksjonalitet er det kommet støtte for sjangere og delvis støtte for tags (i.e. badges med farge). Jeg har også lagt til mulighet for å se slettede bøker i Admin og se leverte bøker i My Books. Også løst div småting som overflow issues. 
</details>
<details open>
<summary>Fredag <sub>28/03</sub></summary>
I dag har drevet med mye finpussing rundtom i appene og fått flere til å teste funksjonalitet. Eksempel på ting jeg har fikset er bl.a. i Search And Borrow er det lagt til Read More funksjonalitet, og har ordnet noe feil null handling. Utenom det har jeg implementert litt ekstra i de dynamiske modalene for å kunne ha custom kolonner slik at f.eks farge kan bli rendret i Add/Manage Tag(s). Har lagt til litt div ikoner rundtom for å gjøre appene litt lettere å forstå. Backend har jeg begynt på reservasjons system og har akkurat skrevet ferdig alt av procedures jeg tror jeg kommer til å trenge, så dette har jo ført til enda en ny tabell; atbl_Library_BooksReservations, som da skal støtte et købasert system for å reservere, med unique constraint på Book_ID - ReserveredBy_ID slik at du ikke reserverer flere ganger på deg selv på en bok, har ikke implementert noe i frontend her enda.
</details>
<details open>
<summary>Lørdag <sub>29/03</sub></summary>
I dag har jeg ferdigstillet reserveringssystemet. I dette ligger all visning i frontend som de forskjellige statusene (om du har reservert, om den er reservert etc.). Utover det har jeg lagt til reserverte bøker i My Borrowed Books, med mulighet til å kansellere reservasjonen ved bruk av en ny procedure som heter CancelReservation. Utover forskjellige tester så virker det som forventet med køsystemet.
</details>
<details open>
<summary>Søndag <sub>30/03</sub></summary>
I dag har jeg startet på API integrasjonen til ISBNdb, for å kunne importere bøker basert på ISBN. Har måttet starte en "7 day free trial", men utover det så er det 15$ i måneden. For det meste gikk det fint hele veien, litt CORS problemer, men de løste jeg for det meste. Om jeg hadde skrevet dette backend hadde jo ikke dette vært et problem, men siden alt dette gjørs via JavaScript så må CORS bli tatt hensyn til. Har klart å få til import av metadata som tittel, beskrivelse etc. Cover trodde jeg skulle gå, men viser seg at endepunktet til ISBNdb ikke støtter CORS på endepunktet som returner bildene, så har måttet sløyfet det. Tror det meste av funksjonalitet er ferdig nå, så planen er å finpusse og dokumentere systemet i morgen.
</details>
<details open>
<summary>Mandag <sub>31/03</sub></summary>
I dag har jeg ferdigstillt appene med litt småforbedringer på designet. Jeg har også ryddet en del i koden for at den skal være med konsistente. Utover det har jeg skrevet første utkast av dokumentasjonen som har tatt mesteparten av dagen.
</details>
<details open>
<summary>Tirsdag <sub>01/04</sub></summary>
tekst
</details>