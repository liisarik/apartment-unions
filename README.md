# apartment-unions
This project investigates the network structure of Estonian apartment unions by using the public data from Äriregister. 

The relationships between apartment unions, their associated companies, and the individual actors involved are quantified and mapped. Network analysis tools, including graph modeling and visualization techniques, are used to highlight key nodes and influential links that shape the operations of these unions. 

The dataset for this project was obtained from the Estonian Business Register (Äriregister) open data portal.
Two primary files are used:

1) Legal Entities Data: A CSV file (ariregistri_valjavote.csv) containing basic registration details for legal entities. This includes the entity's name (nimi), unique registry code (ariregistri_kood), legal form (ettevotja_oiguslik_vorm), status (ettevotja_staatus_tekstina), registration date (ettevotja_esmakande_kpv), and address information (ettevotja_aadress, asukoha_ehak_tekstina). To continue with the data relevant to this project, filtering was done on the Unions to retain only entries where the legal form (ettevotja_oiguslik_vorm) was 'Korteriühistu' (Apartment Union). This resulted in a dataset of 25,156 apartment unions.
   
2) Related Persons Data: A JSON file (ettevotja_rekvisiidid__kaardile_kantud_isikud.json) detailing individuals and potentially other legal entities associated with registered entities. For each associated entity, it lists their role (isiku_roll_tekstina), name (eesnimi, nimi_arinimi), type (isiku_tyyp - 'F' for physical person, 'J' for legal entity), and a unique identifier (isikukood_hash for individuals). It is possible to link these associated persons/entities back to the primary legal entity via the ariregistri_kood.

