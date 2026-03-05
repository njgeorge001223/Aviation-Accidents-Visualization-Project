![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/1ca02e8d-bd3c-4e10-8361-819ab8cec8b0)

----

# **Fatal Skies: A Half-Century of Aviation Accident Data, Visualized**

---

## **Project Overview**

Commercial aviation is one of humanity's most consequential technological achievements — and one of its greatest safety success stories. Yet that story is incomplete without an honest accounting of the accidents that drove each hard-won improvement. This project conducts a comprehensive analysis of more than 50 years of fatal aviation accident data (1970–2022), examining how fatalities vary across countries, aircraft types, operators, flight phases, and decades — and delivering its findings through a suite of three interactive, browser-based visualization tools built on a custom ETL pipeline.

Three guiding questions shaped the investigation: Where are aviation accidents likely to occur? Are there certain airlines or aircraft types with disproportionately high fatality counts? And are there identifiable outside factors — political, cultural, or operational — influencing these trends?

---

## **Landing Page: Context and Framework**

<img width="1106" alt="Screenshot 2023-11-09 at 1 06 18 PM" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/a488b3da-c6d0-4d8f-812f-66da8491057a">

The project's landing page establishes the analytical and historical foundation before directing users into the interactive tools. Three components anchor this page.

The Safety Risk Management (SRM) flowchart on the left maps the structured process by which aviation safety risks are identified, assessed, and controlled — from initial system analysis through hazard identification, risk assessment, corrective action, and conformance verification. This framework contextualizes the entire analysis: the data being visualized is not merely historical record, but the raw material of an ongoing safety management system designed to prevent future fatalities.

The central panel introduces the six goals of the Global Aviation Safety Plan (GASP) 2020–2022 edition, sourced from ICAO. These goals — continuous reduction of operational safety risks, strengthened state oversight, effective State Safety Programmes, regional collaboration, expanded industry programme use, and adequate infrastructure — provide the international policy framework within which the data trends must be interpreted. An improvement in fatality statistics is not accidental; it reflects decades of coordinated global safety effort aligned with exactly these objectives.

The aircraft history timeline at the bottom traces aviation's technological evolution from the 1783 hot air balloon through Da Vinci's conceptual flying machine, Cayley's gliders, the Wright Flyer, the Heinkel He 178 (the world's first jet aircraft), the de Havilland DH.106 Comet, the Boeing 747, the Aérospatiale/BAC Concorde, the Boeing 777, the Martin F-22 Raptor, and the Airbus A380. This timeline matters analytically: the aircraft types that appear most frequently in the fatality data are not modern — they are largely mid-20th-century designs whose safety profiles reflect the engineering and operational standards of their era. The timeline makes this generational context immediately legible.

---

## **Toolkit 1: Aviation Accidents Worldwide Visualization Toolkit**

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/811b062a-d574-4d0e-807e-388ffe3443f0)

The Visualization Toolkit renders the complete 1970–2022 accident record as a global scatter map on a Dark Map base layer, with each accident represented as a circle marker. Marker size encodes total fatalities and marker color encodes fatality count using a five-tier gradient: green (1–40), yellow-green (40–80), yellow-orange (80–120), orange-red (120–160), dark red (160–200), and the deepest red for events exceeding 200 fatalities.

The global view reveals the world's aviation fatality geography with immediate clarity. The densest concentrations of markers — and the largest, darkest circles — are clustered in three primary zones: the former Soviet Union and Russia, spanning from Eastern Europe through Central Asia; the Middle East, South Asia, and the Indian Subcontinent; and Southeast Asia and the Western Pacific. Western Europe and North America show numerous smaller green markers but very few large or dark circles, reflecting the progressive safety improvements achieved in those regulatory environments over the 52-year period.

The single largest circle on the map — a deep red marker positioned over Russia or the Central Asian corridor — likely represents one of the catastrophic Aeroflot accidents of the Soviet era, when single events could produce fatality counts exceeding 200. The contrast between these large Soviet-era markers and the predominantly small green markers scattered across the United States and Western Europe is one of the most visually striking features of the toolkit and one of its most analytically significant messages: geography, regulatory environment, and era are all powerful determinants of accident severity.

The toolbar across the top provides eight filtering dimensions — start year, end year, aircraft type, aircraft operator, aircraft damage, flight phase, nature of flight, and location (country) — enabling users to interrogate any specific combination of variables. The layer panel on the right allows switching between Dark, Satellite, Outdoors, and Grayscale base maps, and toggling the Departure Airports and Destination Airports overlays alongside the Accidents layer — making it possible to visually correlate accident locations with their origin and destination airports.

---

## **Toolkit 2: Aviation Accidents Worldwide Heatmap Toolkit**

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/cb121ea0-def8-4656-b24b-40da1dda95f1)

The Heatmap Toolkit reframes the same accident data through a spatial density lens rather than individual event encoding, aggregating accident locations into a continuous color gradient that reveals geographic concentration patterns invisible in the scatter map. Blue pin markers show individual accident locations, while the heatmap gradient beneath them — transitioning from cool blue through green, yellow, orange, and into deep red — highlights the zones of highest historical accident density.

The heatmap's most striking feature is the two dominant red-orange heat corridors that dominate the visualization. The first stretches across the Americas from Alaska and western Canada down through the continental United States, Mexico, Central America, and into northwestern South America — the entire western hemisphere's most heavily trafficked flight corridor, including the routes where both volume and, historically, regulatory variance have been highest. The second and more intense corridor sweeps across Europe, the Mediterranean, the Middle East, and South Asia — from the United Kingdom and Western Europe through Turkey, Iran, India, and into Southeast Asia — encompassing the most historically volatile combination of high traffic volume and variable safety standards on the planet.

The African continent presents a geographically diffuse but notable pattern: scattered orange and yellow clusters across sub-Saharan Africa, the Horn of Africa, and the Congo Basin indicate persistent accident concentrations in regions characterized by challenging terrain, limited air traffic control infrastructure, and aging aircraft fleets. The Pacific Ocean, predictably, is largely clear — the sparse long-haul routes over the open ocean represent some of aviation's safest corridors in terms of accident density.

The heatmap's filter toolbar mirrors the Visualization Toolkit's controls, enabling the same multi-dimensional filtering. This parallel architecture means users can switch between the precise event-level detail of the scatter map and the spatial density perspective of the heatmap while applying identical filter combinations — a deliberate design choice that makes the two tools analytically complementary.

---

## **Toolkit 3: Aviation Accidents Worldwide Dashboard**

<img width="1679" alt="Screenshot 2023-11-05 at 12 31 54 PM" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/b7e7b9e4-fe96-4542-8ad0-e0901e00a27c">

The Dashboard synthesizes multiple analytical dimensions into a single, coordinated view, combining a geographic composition chart, a flight phase breakdown, a fatality-by-category bar chart, and an individual accident detail panel within a unified interface.

The central bubble chart — Aviation Accidents Geographical Composition — plots each accident by its geographic coordinates (longitude on the x-axis, latitude on the y-axis), with bubble size encoding fatality count and bubble color encoding a categorical variable. The chart's most visually striking feature is the large cluster of overlapping bubbles centered near longitude 0–50 and latitude 0–50 — the geographic zone encompassing Africa, the Middle East, and South Asia — where a dense concentration of accidents of varying sizes creates a complex, layered composition. A second cluster of large blue bubbles appears in the negative longitude region (the Americas), while smaller clusters are visible in the positive longitude, high latitude zone (Russia and Central Asia).

The Flight Phase vs. Fatalities donut chart on the right — shown here for the 1970–1992 subset — reveals that the en route (ENR) phase accounts for the largest single share of fatalities at 49.9%, followed by approach (APR) at 33.6%. Initial climb contributes 6.99%, takeoff 4.61%, landing 3.69%, with maneuvering, standing, and unknown phases accounting for less than 1% each. This distribution has important safety implications: the two highest-fatality phases — en route and approach — represent the periods when full passenger loads are aboard and catastrophic structural failures, weather events, controlled flight into terrain, and navigational errors carry the highest consequences.

The Fatalities vs. Aircraft Type bar chart at the bottom spans the full alphabet of aircraft types, with each bar representing total fatalities across all accidents involving that type. The chart is extremely dense — reflecting the diversity of aircraft types in the 52-year record — but several tall bars stand out visually even at this scale, consistent with the dedicated aircraft type analysis shown in Image 7.

---

## **Long-Term Fatality Trend**

<img width="617" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/177588e2-cf44-4a1d-8b06-e48e3e4234dc">

The Total Aviation Fatalities vs. Year chart (1970–2022) is perhaps the single most important visualization in the entire project, and its message is both clear and striking. Starting from a baseline of approximately 340 fatalities in 1970, the trend line is characterized by high volatility — dramatic year-over-year swings driven by individual catastrophic events — but the underlying directional trend is unmistakably downward.

The peak years are concentrated in the late 1970s and late 1980s. The 1979 peak reaches approximately 614 fatalities, driven almost certainly by a combination of high-profile Soviet accidents and the worst U.S. aviation disaster of that era. The 1988–1989 peak reaches approximately 628 — the single highest year in the entire dataset — likely reflecting the convergence of the Lockerbie bombing (270 fatalities), the Ramstein air show disaster, and a cluster of other major accidents in that period. From this peak, the trend descends consistently and dramatically: by the mid-1990s, annual fatalities had fallen to the 100–200 range; by the late 2000s and early 2010s, several years recorded fewer than 50 fatalities; and from 2015 through 2019, the record reached its lowest sustained levels, with multiple years approaching zero.

The sharp spike in 2022 — rising to approximately 175 fatalities — is the most recent and concerning data point. It represents a meaningful departure from the near-zero levels of 2018–2020 and is almost certainly attributable in significant part to a single catastrophic event: the China Eastern Airlines Flight MU5735 crash in March 2022, which killed all 132 people on board and was the deadliest Chinese aviation accident in nearly three decades.

The overall arc of this chart is one of the most compelling data stories in the project: a 50-year safety transformation that reduced annual aviation fatalities by roughly 90% from their peak, driven by improvements in aircraft design, air traffic control, crew training, regulatory oversight, and international safety cooperation — then punctuated by a recent reversal that demands explanation.

---

## **Flight Phase Analysis**

<img width="623" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/c304e4ad-a0b3-4dad-b50d-1521ff48f053">

The Fatalities per Flight Phase pie chart (1970–2022, filtered to accidents with more than 10 fatalities) provides a definitive breakdown of when during a flight fatal accidents are most likely to occur. En route (ENR) accounts for 45.6% of fatalities — nearly half the total — confirming that the cruising phase, despite being statistically the safest per-minute period, produces the most fatalities in absolute terms simply because it encompasses the longest portion of any flight and because catastrophic structural failures, weather encounters, and deliberate acts during this phase leave little opportunity for survival. Approach (APR) accounts for 35.4%, reflecting the well-documented dangers of the descent and final approach phases: controlled flight into terrain, instrument approach errors, and runway environment confusion are among aviation's most persistent fatal accident categories.

Together, en route and approach account for over 81% of all fatalities in the dataset — a finding with direct implications for where safety investment, training emphasis, and regulatory attention should be concentrated. Initial climb (ICL) at 6.4%, takeoff (TOF) at 6.3%, and landing (LDG) at 6.2% account for roughly equal and modest shares, while maneuvering (MNV) contributes just 0.1% — a negligible fraction consistent with the rarity of intentional maneuvering flights among commercial passenger operations.

---

## **Aircraft Type Analysis**

<img width="506" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/a99ffbe9-7e5e-4052-9b90-c22ca7ac582c">

The Fatalities per Aircraft Type chart (1970–2022, filtered to types with more than 100 fatalities) identifies the aircraft designs most associated with fatal outcomes across the 52-year record. The Tupolev TU-154 leads with approximately 487 fatalities — the highest of any aircraft type in the dataset. A Soviet-era narrow-body trijet that entered service in 1972 and remained in operation well into the 2010s, the TU-154 accumulated its fatality record across decades of operation under Soviet, Russian, and Eastern Bloc carriers in an environment where maintenance standards, crew training, and air traffic control infrastructure were substantially below Western norms. The Lockheed L-1011 TriStar follows with approximately 437 fatalities, and the Boeing 727 with approximately 389 — both legacy wide-bodies and narrow-bodies of 1960s and 1970s vintage whose accident records reflect the lower safety standards of that era rather than any inherent design deficiency relative to their contemporaries.

The Boeing 737's presence on this chart at approximately 245 fatalities — a modern, continuously updated aircraft that has been the world's most widely operated commercial jet for decades — reflects both its extraordinary volume of operations and the specific issues that produced the 737 MAX accidents in 2018 and 2019. The Airbus A300 at approximately 293 fatalities and the Airbus A320 at approximately 260 represent similar patterns: high-volume modern aircraft whose fatality records are a function of operational scale as much as design risk.

The implications of this chart require careful interpretation. Raw fatality counts by aircraft type do not control for total flight hours, number of aircraft in service, or era of operation. The TU-154's lead reflects the combination of a very large Soviet and Russian operational fleet, decades of service in a challenging regulatory environment, and the era in which most of its accidents occurred — not a structural safety inferiority to equivalent Western aircraft of the same period.

---

## **Nature of Flight Analysis**

<img width="404" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/68cd9132-4722-4b22-82f0-64780efb5a87">

The Fatalities per Nature of Flight pie chart (1970–2022, filtered to categories with more than 100 fatalities) reveals that domestic scheduled passenger service accounts for 53.0% of all fatalities in the dataset — the dominant category by a substantial margin. International scheduled passenger service contributes 31.3%, and domestic non-scheduled passenger flights add 8.4%, while international non-scheduled passenger operations account for 7.2%.

The dominance of domestic scheduled passenger service in the fatality record is partly a function of volume — domestic passenger flights vastly outnumber all other flight categories in total operations — but it also reflects a geographic concentration effect. Many of the deadliest decades in the dataset were dominated by Soviet domestic operations, which were technically domestic scheduled passenger service despite involving routes spanning thousands of miles across eleven time zones. The Soviet airline Aeroflot alone operated the world's largest domestic network throughout the 1970s and 1980s, and its accident record during that period contributes substantially to this category's dominance.

The near-equal shares of domestic and international scheduled passenger in the dataset also reflect a well-known pattern in aviation safety research: domestic operations in countries with less developed regulatory infrastructure carry meaningfully higher accident rates than international operations by the same carriers, because international routes are subject to higher scrutiny from foreign aviation authorities and international safety oversight bodies.

---

## **Country-Level Analysis: The 2010s**

<img width="432" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/c4949211-48c4-4547-b81b-040a596b9078">

The Fatalities per Country chart for the 2010s (filtered to countries with more than 30 fatalities in the decade) produces a notably short list: Russia leads with approximately 63 fatalities, followed by Taiwan with 48, Afghanistan with 44, and Namibia with 33. The brevity of this list — just four countries exceeding the 30-fatality threshold in an entire decade — is itself a powerful testament to how dramatically global aviation safety had improved by the 2010s relative to the catastrophic multi-hundred-fatality years of the 1970s and 1980s.

Russia's continued presence at the top of the country rankings in the 2010s, despite the enormous improvements in global aviation safety, reflects a persistent pattern of structural challenges: aging legacy aircraft still in service on domestic routes, complex terrain, weather extremes, and the lingering effects of regulatory and cultural practices that have proven more resistant to reform than the technical aspects of aviation safety. Afghanistan's appearance in the ranking is consistent with the geopolitical volatility and infrastructure limitations of that country throughout the decade, including security threats that contributed to several fatal incidents. Taiwan's relatively high figure in the 2010s is largely attributable to TransAsia Airways accidents in 2014 and 2015, which together killed over 100 people and ultimately led to the carrier's shutdown. Namibia's presence reflects a small number of high-fatality incidents in a country with limited aviation infrastructure.

---

## Summary of Key Findings

Taken together, the three toolkits and nine visualizations converge on a set of clear and significant conclusions.

Aviation has achieved a remarkable safety transformation over the past 50 years. Annual fatalities fell by approximately 90% from their late-1980s peak to the record lows of the mid-2010s — one of the most successful long-term safety improvement trajectories of any major transportation system. The downward trend is real, sustained, and global.

Geography remains a powerful determinant of aviation risk. The former Soviet Union, Russia, the Middle East, South Asia, and sub-Saharan Africa have consistently produced disproportionate shares of the fatality record. Western Europe and North America, despite operating the world's busiest airspace, account for a relatively small share of fatalities across the 52-year period.

En route and approach are the deadliest flight phases, accounting together for over 80% of all fatalities. Safety investment and training emphasis concentrated in these phases would address the large majority of the remaining risk.

The aircraft types with the highest historical fatality counts are predominantly Soviet-era and 1960s-1970s Western designs. The persistence of these legacy aircraft in service in certain regions long after their Western counterparts were retired drove a significant portion of the late-20th-century fatality record.

Domestic scheduled passenger service accounts for the majority of fatalities — a finding that reflects both operational volume and the disproportionate risk profile of domestic operations in countries with less developed regulatory infrastructure.

The 2022 spike demands attention. After reaching near-zero levels in the late 2010s, fatalities surged in 2022, driven substantially by the China Eastern Airlines disaster. The identification of China Eastern as the carrier with the highest recent fatalities — in an era of far safer aircraft and practices — points toward operational and cultural factors that technical and regulatory improvements alone cannot address.

---

## Limitations and Future Directions

The analysis is appropriately bounded by its data. Fatality counts without normalization against total flight hours or passenger miles cannot produce accident rates — the more analytically rigorous metric for comparing safety performance across operators, aircraft types, and countries of different operational scales. A critical next step is to pair this fatality dataset with total flight data to produce rate-based metrics, which would substantially sharpen the comparative conclusions about which operators, aircraft types, and regions carry the highest genuine risk.

Additionally, the identification of outside factors — terrorism, political instability, and cultural practices — as potential contributors to accident trends warrants systematic quantitative investigation rather than qualitative observation. Correlating accident rates with indices of political stability, regulatory development, and cultural attitudes toward safety reporting could produce actionable insights for international aviation safety policy.

The toolkit suite developed here is a powerful and flexible foundation for that deeper investigation — and a compelling demonstration that half a century of fatal accident data, properly organized and visualized, has a great deal left to say.


---------

Air travel stands as an undeniable revolution in the transportation sector, delivering a multitude of invaluable advantages: unprecedented speed, unparalleled global connectivity, and a continuous drive for innovation. Nevertheless, the aviation industry encounters its fair share of challenges, especially concerning the issue of safety. In this project, we delve into the intricate tapestry of aviation safety, exploring how fatalities from accidents vary among different countries, aircraft types, and operators in a comprehensive analysis of over 50 years of aviation accident data (1970-2022). 

Questions we considered:
* Where are aviation accidents likely to occur?
* In recent years, are there certain airlines that have more crashes than others?
* Are there possible outside factors affecting these trends?

To find the answers to our questions, we obtained the requisite information by means of a customized Extract-Transform-Load process. The procurement of aviation accident information began with web scraping sources on the Internet.  Subsequently, an initial review of the information showed important details mixed together with irrelenant ones in various and inconsistent forms.  To compensate for this obstacle, we implemented algorithms to parse text for important specifics, verify or augment information using APIs and other sources, and standardize the data.  After placing the cleaned information in an SQLite database, a Flask API provides it to front-end applications in an efficent and effective manner. To accomplish our goal of interactive visualization, we employed certain technologies -- D3, JSON, JS, Plotly, Bootstrap, among others -- and aimed to create an informative representation of historical aviation accident data, which could allow stakeholders to uncover patterns, trends, and insight.

----

## Landing Page:

<img width="1106" alt="Screenshot 2023-11-09 at 1 06 18 PM" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/a488b3da-c6d0-4d8f-812f-66da8491057a">

## Aviation Accidents Worldwide Visualization Toolkit:

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/811b062a-d574-4d0e-807e-388ffe3443f0)

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/e670cc73-e09b-4263-8583-b3ba341f5175)

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/d91573cd-9001-4250-b707-5c59084e43d4)

## Aviation Accidents Worldwide Heatmap Toolkit:

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/5acddd9f-f938-4ff6-9072-7a10d97685a9)

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/cb121ea0-def8-4656-b24b-40da1dda95f1)

![image](https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/a7aa13af-9682-4d26-ae4f-0cfe29c80977)

## Aviation Accidents Worldwide Dashboard:

<img width="1679" alt="Screenshot 2023-11-05 at 12 31 54 PM" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/b7e7b9e4-fe96-4542-8ad0-e0901e00a27c">

<img width="1679" alt="Screenshot 2023-11-05 at 12 33 55 PM" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/e2d62e39-c49e-4403-a3b1-b50512384ae4">

To best convey our findings, we summarized them in a series of visual aids. First, our analysis revealed a downward trend in fatalities from aviation accidents over the last fifty years. 

<img width="617" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/177588e2-cf44-4a1d-8b06-e48e3e4234dc">

This downward trend also manifested itself in a lower average casualty rate per flight and lower and narrower casualty rate distributions.

<img width="741" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/c52b3b28-3b31-412e-9f4a-1a236af69550">

<img width="741" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/8df7472d-6f0c-4cd7-9632-ea08fb3c48b9">

Overall and most recently, accidents occur when the aircraft is en route or approaching its destination.

<img width="623" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/c304e4ad-a0b3-4dad-b50d-1521ff48f053">

In the last fifty years, Aeroflot has been the airline with the highest fatalities although these accidents primarily happened during the Soviet era in the 1970s and 1980s. In the last few years, China Eastern Airlines has had a troublingly high number of fatalities in a time of safer aircraft and practices.

<img width="404" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/61ab3880-a4fb-448b-80f6-fc201ac90587"><img width="404" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/40821864-b1c8-4af3-ba87-73dc3aed0e54">

The aircraft most prone to fatalities from aviation accidents is the Tupolev TU-154, a Soviet era aircraft, followed by the Lockheed L-1011 and Boeing 727.  In the last twenty years or so the Boeing 737 has been the leader in this infamous category.

<img width="404" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/23a05db8-b849-430a-a957-604f2b61aa64">

<img width="506" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/a99ffbe9-7e5e-4052-9b90-c22ca7ac582c">

<img width="404" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/09da2831-5195-486e-a471-1efbd0d942d3">

In any period, domestic scheduled passenger flights are most likely to have fatalities from aviation accidents followed by international scheduled passenger flights.

<img width="720" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/9d4720a7-4462-48b0-a4e8-32fc00491566">

In the last few years, certain Chinese departure and destination airports have had the largest proportion of accidents.

<img width="404" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/68cd9132-4722-4b22-82f0-64780efb5a87"><img width="404" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/e7f957f4-c01c-4e06-ade3-e789a17c3a08">

Also, Russia has consistently been the a location for high numbers of fatalities even though China has lately taken on that mantle.

<img width="432" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/c4949211-48c4-4547-b81b-040a596b9078">

<img width="432" alt="image" src="https://github.com/njgeorge000158/Aviation-Accidents-Visualization-Project/assets/137228821/d1812e69-2394-4c4b-b528-629522cc16b8">

----

Ultimately, we could not accurately predict the locations of aircraft accidents only the likelihood based on past events and those parameters change from decade to decade, but we did observe some trends.  During the last few years, China Eastern Airlines has experienced the highest number fatalities. Currently, possible outside factors for these aviation fatalities include terrorism, political upheaval, and cultural practices. In any case, the next China Eastern Airlines' domestic passenger flight from Kunming Changshui International Airport to Guangzhou Baiyun International Airport on a Boeing 737 should likely be avoided! This project is a positive first step toward understanding aviation accidents, and, in the future, these fatalities should be compared with total flight data to render percentages as the metric for a clearer picture of the situation.

----

## Copyright

Nicholas J. George © 2023. All Rights Reserved.
