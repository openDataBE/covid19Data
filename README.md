# SARS-CoV-2 data (Canton of Bern) reported by the Federal Office of Public Health FOPH and "Gesundheits-, Sozial- und Integrationsdirektion (GSI) des Kantons Bern".

## Aim

The aim of this repository is to provide open government datasets for SARS-CoV-2 related data (Canton Bern) reported by the Federal Office of Public Health FOPH and "Gesundheits-, Sozial- und Integrationsdirektion (GSI) des Kantons Bern". Since Jun 8, 2020 most cantons report case numbers at least once or twice a week. Updates of cantonal case numbers during weekends are infrequent.

If you have any questions, please don't hestitate to contact us: <br>
- SARS-CoV-2 Hotline Canton Bern: +41 31 636 87 87 <br>
- [info@gsi.be.ch](mailto:info@info.be.ch) <br>

## List of open government datasets¹ and non-published datasets in this repository

**Federal Office of Public Health FOPH** <br>
- [Negative Labortests] (not accessible) <br>
- [Labortests] (not accessible) <br>
- [Falldetails] (not accessible) <br>

**Federal Statistical Office**
- [Swiss official commune register¹] (https://www.bfs.admin.ch/bfs/de/home/grundlagen/agvch.html) <br>
- [Regionalportraets 2020: Kennzahlen aller Gemeinden¹] (https://www.bfs.admin.ch/bfs/de/home/statistiken/regionalstatistik/regionale-portraets-kennzahlen/gemeinden.assetdetail.11587763.html) <br>

**Canton Bern** <br>
- [Contact Tracing Data - TRACY] (not accessible) <br>
- [Hospital Data - SPA] (not accessible) <br>

## Table: 1. Tests und laborbestätigte Fälle

**General description** <br>
The table shows newly reported tests and cases.


**Data** <br>

>**Negative Labortests (not accessible); Labortests (not accessible); Falldetails (not accessible)** <br>
>*Description:* Snapshot of the difference from the last report of data: The values in this table show the daily newly reported numbers of tests and laboratory-confirmed cases respectively fatalities inculding positivity rate. <br>
>*Spatial unit:* Canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.<br>


**Metadata**

| Field Name                                              | Description                                | Format     | Example   | Source                                                                  |
|---------------------------------------------------------|--------------------------------------------|------------|-----------|-------------------------------------------------------------------------|
| __falleingangsdatum\_BAG__                              | Case report date.                          | DD.MM.YYYY |01.05.2021 | Falldetails                                                             |
| __Durchgefuehrte\_Tests__                               | Number of tests conducted.                 | Number     |5620       | Labortests (not accessible); Falldetails (not accessible)               |
| __Neue\_laborbestaetigte\_Faelle__                      | New laboratory-confirmed cases.            | Number     |126        | Falldetails                                                             |
| __Positivitaetsrate__                                   | Positivity rate.                           | Number     |12.5%      | Labortests (not accessible); Falldetails (not accessible); (calculated) |
| __Neue\_laborbestaetigte\_Todesfaelle__                 | New laboratory-confirmed fatalities.       | Number     |0          | Falldetails                                                             |


**Empty values**

| Value    | Meaning |
|----------| --------|
|zero      | Zero tests/cases are reported.|


## Table: 2. COVID-19 Patient*innen im Spital

**General description** <br>
The table shows values on currently hospitalized COVID-19 patients.

**Data** <br>

>**Hospital Data - SPA** <br>
>*Description:* Snapshot on currently hospitalized COVID-19 patients: The values in this table show the current situation of COVID-19 hospitalized patients in the canton of Bern in terms of hospitalization category. <br>
>*Spatial unit:* Canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on "Gesundheits-, Sozial- und Integrationsdirektion (GSI) des Kantons Bern".<br>
>*Update periodicy:* This csv file is updated once per week - usually on Wednesdays. <br>


**Metadata**

| Field Name                                              | Description                                                    | Format     | Example     | Source             |
|---------------------------------------------------------|----------------------------------------------------------------|------------|-------------|--------------------|
| __datum__                                               | Report date.                                                   | DD.MM.YYYY |01.05.2021   | Hospital Data - SPA|
| __personen\_hospitalisiert__                            | Number of hospitalized COVID-19 patients.                      | Number     |145          | Hospital Data - SPA|
| __auf\_normaler\_Bettenstation__                        | Number of COVID-19 patients in regular wards.                  | Number     |92           | Hospital Data - SPA|
| __auf\_intensivpflegestation\_unbeatmet__               | Number of COVID-19 patients in intensive care units.           | Number     |30           | Hospital Data - SPA|
| __auf\_intensivpflegestation\_beatmet__                 | Number of COVID-19 patients in intensive care unit respirated. | Number     |23           | Hospital Data - SPA|


**Empty values**

| Value    | Meaning |
|----------| --------|
|zero      | Zero patients are reported.|



## Table: 3. Contact Tracing

**General description** <br>
The table shows values for persons currently in quarantine respectively isolation.

**Data** <br>

>**Contact Tracing Data - TRACY; Falldetails (not accessible)** <br>
>*Description:* Snapshot on the current contact tracing situation and fatalities: The values in this table show the current situation of persons in quarantine respectively isolation and the total fatalities. <br>
>*Spatial unit:* Canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on "Gesundheits-, Sozial- und Integrationsdirektion (GSI) des Kantons Bern".<br>
>*Update periodicy:* This csv file is updated daily - usually in the mornings. <br>


**Metadata**

| Field Name                                              | Description                                                       | Format     | Example       | Source                                    |
|---------------------------------------------------------|-------------------------------------------------------------------|------------|---------------|-------------------------------------------|
| __datum__                                               | Case report date.                                                 | DD.MM.YYYY |01.05.2021     | Contact Tracing Data - TRACY              |
| __personen\_in\_quarantaene__                           | Number of persons in quarantine.                                  | Number     |2000           | Contact Tracing Data - TRACY              |
| __personen\_in\_isolation__                             | Number of persons in isolation.                                   | Number     |200            | Contact Tracing Data - TRACY              |


**Empty values**

| Value    | Meaning |
|----------| --------|
|zero      | Zero persons are reported.


## Chart: 4. Inzidenzen (Gemeinde)

**General description** <br>
The chart shows the current 7-day incidence per 100'000 inhabitants per municipality in the canton of Bern. Municipalities with <= 500 inhabitants are not included in the report.

**Data** <br>

>**Falldetails (not accessible); Swiss official commune register¹; Regionalportraets 2020: Kennzahlen aller Gemeinden¹** <br>
>*Description:* Snapshot of the previous day: listing of all municipalities in the canton of Bern with at least one (1) case in the last 14 days, including the 7- incidence (per 100'000 inhabitants)<br>
>*Spatial unit:* Municipality in the canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.) <br>


**Metadata**

| Field Name                                              | Description                                | Format     | Example       | Source                                             |
|---------------------------------------------------------|--------------------------------------------|------------|---------------|----------------------------------------------------|
| __Datum__                                               | Case report date                           | DD.MM.YYYY |01.05.2021     | Falldetails                                        |
| __gemeinde__                                            | Municipality                               | Text       |Orpund         | Falldetails                                        |
| __bfs_nummer__                                          | BFS Number per municipality                | Number     |744            | Swiss official commune register¹                   |
| __einwohnerzahl__                                       | Number of inhabitants per municipality     | Number     |2800           | Regionalportraets 2020: Kennzahlen aller Gemeinden¹|
| __7\_d\_inzidenz__                                      | 7-day incidence per 100'000                | Number     |71.43          | calculated                                         |

**Empty values**

| Value    | Meaning |
|----------| --------|
|empty     | Zero cases are reported.


## Chart: 5. Inzidenzen (Verwaltungskreis)

**General description** <br>
The chart shows the change in the current 7-day respectively 14-day incidence to the last 7-day respectively 14-day incidence per 100'000 inhabitants and absolute per region in the canton of Bern.


**Data** <br>

>**Falldetails (not accessible); Swiss official commune register¹; Regionalportraets 2020: Kennzahlen aller Gemeinden¹** <br>
>*Description:* Snapshot of the previous day: listing of all municipalities in the canton of Bern with at least one (1) case in the last 14 days, including the 7- and 14-day incidence (per 100'000 inhabitants and absolute) and the respective percentage change. <br>
>*Spatial unit:* Region in the canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.) <br>


**Metadata**

| Field Name                                              | Description                                | Format     | Example    | Source                                                          |
|---------------------------------------------------------|--------------------------------------------|------------|------------|-----------------------------------------------------------------|
| __falleingangsdatum\_BAG__                              | Case report date                           | DD.MM.YYYY |01.05.2021  | Falldetails                                                     |
| __Verwaltungskreis__                                    | Region                                     | Text       |Thun        | Falldetails (matched with Swiss official commune register¹)     |
| __Einwohnerzahl\_Verwaltungskreis__                     | Number of inhabitants per region           | Number     |107029      | Regionalportraets 2020: Kennzahlen aller Gemeinden¹ (calculated)|
| __BFS-Nummer\_Verwaltungskreis__                        | BFS Number per region                      | Number     |247         | Swiss official commune register¹                                |
| __14\_tages\_inzidenz__                                 | 14-day incidence absolute                  | Number     |188         | calculated                                                      |
| __14\_tages_inzidenz\_pro\_100k\_einwohner__            | 14-day incidence per 100'000               | Number     |175.65      | calculated                                                      |
| __vorletzte\_7_tages\_inzidenz__                        | Penultimate 7-day incidence absolute       | Number     |111         | calculated                                                      |
| __vorletzte\_7\_tages\_inzidenz\_pro\_100k\_einwohner__ | Penultimate 7-day incidence per 100'000    | Number     |103.71      | calculated                                                      |
| __7\_tages\_inzidenz__                                  | 7-day incidence absolute                   | Number     |77          | calculated                                                      |
| __7\_tages\_inzidenz\_pro\_100k\_einwohner__            | 7-day incidence per 100'000                | Number     |71.94       | calculated                                                      |
| __veraenderung\_7\_tages\_inzidenz__                    | percentage change 7-day                    | Number     |-30.63      | calculated                                                      |
| __faktor\_veraenderung\_7\_tages\_inzidenz__            | factor change 7-day                        | Number     |0.47        | calculated                                                      |


**Empty values**

| Value    | Meaning |
|----------| --------|
|empty     | Zero cases are reported.|


## Chart: 6. Demografie / Gender

**General description** <br>
The chart shows the age distribution of laboratory-confirmed cases.


**Data** <br>

>**Falldetails (not accessible)** <br>
>*Description:* Chronological listing of the age distribution of all laboratory-confirmed cases since the beginning of the COVID-19 pandemic.<br>
>*Spatial unit:* Canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.<br>


**Metadata**

| Field Name                                      | Description                                                   | Format     | Example     | Source                             |
|-------------------------------------------------|---------------------------------------------------------------|------------|-------------|------------------------------------|
| __jahr__                                        | Case report year                                              | Number     |2021         | Falldetails                        |
| __kw__                                          | Case report week                                              | Number     |18           | Falldetails (calculated)           |
| __alterskategegorie__                           | Age by decade. Up to 100+. Invalid ages are assigned to #null | Text       |20-29        | Falldetails (calculated)           |
| __anzahl_falleingaenge__                        | Number of laboratory-confirmed cases - newly reported.        | Number     |2            | Falldetails                        |


**Empty values**

| Value                    | Meaning                                      |
|--------------------------| ---------------------------------------------|
|[Missing age bracket]     | No patients in this age range were reported. |