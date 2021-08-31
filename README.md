# SARS-CoV-2 data (Canton of Bern) reported by the Federal Office of Public Health FOPH and "Gesundheits-, Sozial- und Integrationsdirektion (GSI) des Kantons Bern".

## Aim

The aim of this repository is to provide open government datasets for SARS-CoV-2 related data (Canton Bern) reported by the Federal Office of Public Health FOPH and "Gesundheits-, Sozial- und Integrationsdirektion (GSI) des Kantons Bern". Since Jun 8, 2020 most cantons report case numbers at least once or twice a week. Updates of cantonal case numbers during weekends are infrequent.

If you have any questions, please don't hestitate to contact us: <br>
- SARS-CoV-2 Hotline Canton Bern: +41 31 636 87 87 <br>
- [info.gsi@be.ch](mailto:info.gsi@be.ch) <br>
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

## Table: 7 Tage Inzidenz (Gemeinde)

**File** [7_d_inzidenz_gemeinde.csv](https://github.com/openDataBE/covid19Data/blob/develop/7_d_inzidenz_gemeinde.csv) <br>

**General description** <br>
The chart shows the current 7-day incidence per 100'000 inhabitants per municipality in the canton of Bern. Municipalities with <= 500 inhabitants are not included in the report.

**Data** <br>
>**Falldetails (not accessible); Swiss official commune register¹; Regionalportraets 2020: Kennzahlen aller Gemeinden¹** <br>
>*Description:* Snapshot of the previous day: listing of all municipalities in the canton of Bern exept municipalities with 500 or less inhabitants, including the 7- incidence (per 100'000 inhabitants)<br>
>*Spatial unit:* Municipality in the canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.<br>


**Metadata**

| Field Name                                              | Description                                | Format     | Example       | Source                                             |
|---------------------------------------------------------|--------------------------------------------|------------|---------------|----------------------------------------------------|
| __datum__                                               | Case report date                           | DD.MM.YYYY |01.05.2021     | Falldetails                                        |
| __gemeinde__                                            | Municipality                               | Text       |Orpund         | Falldetails                                        |
| __bfs_nummer__                                          | BFS Number per municipality                | Number     |744            | Swiss official commune register¹                   |
| __einwohnerzahl__                                       | Number of inhabitants per municipality     | Number     |2800           | Regionalportraets 2020: Kennzahlen aller Gemeinden¹|
| __7\_d\_inzidenz__                                      | 7-day incidence per 100'000                | Number     |71.43          | calculated                                         |

**Empty values**

| Value                  | Meaning |
|------------------------| --------|
|[missing municipality]  | Municipalities with 500 or less inhabitants.|
|[0]  | Zero cases were reported for this municipality within the last 7 days.|

## Table: 7 Tage Inzidenz (Verwaltungskreis)

**File** [7_d_inzidenz_verwaltungskreis.csv](https://github.com/openDataBE/covid19Data/blob/develop/7_d_inzidenz_verwaltungskreis.csv) <br>

**General description** <br>
The chart shows the current 7-day incidence per 100'000 inhabitants per region in the canton of Bern.


**Data** <br>

>**Falldetails (not accessible); Swiss official commune register¹; Regionalportraets 2020: Kennzahlen aller Gemeinden¹** <br>
>*Description:* Snapshot of the previous day: listing of all regions in the canton of Bern.<br>
>*Spatial unit:* Region in the canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.<br>


**Metadata**

| Field Name                                              | Description                                | Format     | Example    | Source                                                          |
|---------------------------------------------------------|--------------------------------------------|------------|------------|-----------------------------------------------------------------|
| __datum__                                               | Case report date                           | DD.MM.YYYY |01.05.2021  | Falldetails                                                     |
| __verwaltungskreis__                                    | Region                                     | Text       |Thun        | Falldetails (matched with Swiss official commune register¹)     |
| __bfs_nummer__                                          | BFS Number per region                      | Number     |247         | Swiss official commune register¹                                |
| __einwohnerzahl__                                       | Number of inhabitants per region           | Number     |107029      | Regionalportraets 2020: Kennzahlen aller Gemeinden¹ (calculated)|
| __7\_d\_inzidenz__                                      | 7-day incidence absolute                   | Number     |188         | calculated                                                      |


**Empty values**

| Value            | Meaning |
|------------------| --------|
|[0]  | Zero cases were reported for this region.|

## Table: Contact Tracing

**File** [contact_tracing.csv](https://github.com/openDataBE/covid19Data/blob/develop/contact_tracing.csv) <br>

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
|[0]     | Zero persons are reported.
|[empty]     | No data provided.

## Table: Demografie / Gender

**File** [demografie.csv](https://github.com/openDataBE/covid19Data/blob/develop/demografie.csv) <br>

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

## Table: COVID-19 Patient*innen im Spital

**File** [spa_auslastung.csv](https://github.com/openDataBE/covid19Data/blob/develop/spa_auslastung.csv) <br>

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

| Field Name                                              | Description                                                             | Format     | Example     | Source             |
|---------------------------------------------------------|-------------------------------------------------------------------------|------------|-------------|--------------------|
| __datum__                                               | Report date.                                                            | DD.MM.YYYY |01.05.2021   | Hospital Data - SPA|
| __personen\_hospitalisiert__                            | Number of hospitalized COVID-19 patients.                               | Number     |145          | Hospital Data - SPA|
| __auf\_normaler\_Bettenstation__                        | Number of COVID-19 patients in regular wards.                           | Number     |92           | Hospital Data - SPA|
| __auf\_intensivpflegestation\_unbeatmet__               | Number of COVID-19 patients in intensive care units.                    | Number     |30           | Hospital Data - SPA|
| __auf\_intensivpflegestation\_beatmet__                 | Number of COVID-19 patients in intensive care unit respirated.          | Number     |23           | Hospital Data - SPA|
| __auf\_intensivpflegestation\_total__                   | Sum of COVID-19 patients in intensive care unit unrespirated/respirated.| Number     |53           | Hospital Data - SPA|
| __vac\_prozent\_personen\_hospitalisiert__              | Percentage of vaccinated, hospitalized COVID-19 patients.               | Number (percent)    |6.5          | Hospital Data - SPA|
| __vac\_prozent\_auf\_normaler\_Bettenstation__          | Percentage of vaccinated, COVID-19 patients in regular wards.           | Number (percent)    |8.3           | Hospital Data - SPA|
| __vac\_prozent\_auf\_intensivpflegestation\_unbeatmet__ | Percentage of vaccinated, COVID-19 patients in intensive care units.    | Number (percent)    |2.1           | Hospital Data - SPA|
| __vac\_prozent\_auf\_intensivpflegestation\_beatmet__   | Percentage of vaccinated, COVID-19 patients in intensive care unit respirated.          | Number (percent)    |3.2           | Hospital Data - SPA|
| __vac\_prozent\_auf\_intensivpflegestation\_total__     | Percentage of vaccinated, COVID-19 patients in intensive care unit unrespirated/respirated.| Number (percent)     |1.2           | Hospital Data - SPA|


**Empty values**

| Value    | Meaning |
|----------| --------|
|[0]      | Zero patients are reported.|

## Table: Total cases

**File** [total_faelle.csv](https://github.com/openDataBE/covid19Data/blob/develop/total_faelle.csv) <br>

**General description** <br>
The table shows the number of total cases and total deaths.

**Data** <br>

>**Falldetails (not accessible)** <br>
>*Description:* Total number of cases and fatalities per day with at least one case or fatality. The table only shows the most recent date in the dataset.<br>
>*Spatial unit:* Canton of Bern<br>
>*Format:* csv<br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.<br>


**Metadata**

| Field Name                                              | Description                                                       | Format     | Example       | Source                                    |
|---------------------------------------------------------|-------------------------------------------------------------------|------------|---------------|-------------------------------------------|
| __datum__                                               | Case report date.                                                 | DD.MM.YYYY |01.05.2021     | Falldetails                               |
| __total\_laborbestaetigte\_faelle__                     | Total number of cases.                                            | Number     |2000           | Falldetails (calculated)                  |
| __total\_todesfaelle__                                  | Total number of fatalities                                        | Number     |200            | Falldetails (calculated)                  |


**Empty values**

| Value              | Meaning                                                |
|--------------------| -------------------------------------------------------|
|[missing date]      | No new cases and fatalities were reported on this day.


## Table: Vortag Fälle

**File** [vortag_faelle.csv](https://github.com/openDataBE/covid19Data/blob/develop/vortag_faelle.csv) <br>

**General description** <br>
The table shows newly reported cases.


**Data** <br>

>**Falldetails (not accessible)** <br>
>*Description:* Snapshot of the difference from the last report of data: The values in this table show the daily newly reported numbers of laboratory-confirmed cases respectively fatalities. <br>
>*Spatial unit:* Canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.<br>


**Metadata**

| Field Name                                              | Description                                | Format     | Example   | Source                                                                  |
|---------------------------------------------------------|--------------------------------------------|------------|-----------|-------------------------------------------------------------------------|
| __datum__                              | Case report date.                          | DD.MM.YYYY |01.05.2021 | Falldetails                                                             |
| __neue\_laborbestaetigte\_Faelle__                      | New laboratory-confirmed cases.            | Number     |126        | Falldetails                                                             |
| __neue\_Todesfaelle__                 | New laboratory-confirmed fatalities.       | Number     |0          | Falldetails                                                             |
| __vac\_prozent\_neue\_laborbestaetigte\_faelle__                 | 7-Day average of vaccinated cases (percent) of new laboratory-confirmed cases        | Number (percent)     |0          | Falldetails                                                             |


**Empty values**

| Value    | Meaning |
|----------| --------|
|zero      | Zero cases are reported.|


## Table: Vortag Tests

**File** [vortag_tests.csv](https://github.com/openDataBE/covid19Data/blob/develop/vortag_tests.csv) <br>

**General description** <br>
The table shows newly reported tests.


**Data** <br>

>**Negative Labortests (not accessible); Labortests (not accessible)** <br>
>*Description:* Snapshot of the difference from the last report of data: The values in this table show the daily newly reported numbers of tests inculding positivity rate. <br>
>*Spatial unit:* Canton of Bern <br>
>*Format:* csv <br>
>*Stability of datasource:* Basically very stable - dependent on Federal Office of Public Health FOPH.<br>
>*Update periodicy:* This csv file is updated once per working day - usually in the morning.<br>


**Metadata**

| Field Name                                              | Description                                | Format     | Example   | Source                                                                  |
|---------------------------------------------------------|--------------------------------------------|------------|-----------|-------------------------------------------------------------------------|
| __datum__                              | Case report date.                          | DD.MM.YYYY |01.05.2021 | Falldetails                                                             |
| __durchgefuehrte\_tests__                               | Number of tests conducted.                 | Number     |5620       | Labortests (not accessible); Falldetails (not accessible)               |
| __positive\_tests__                               | Number of positive tests.                 | Number     |620       | Labortests (not accessible); Falldetails (not accessible)               |
| __positivitaetsrate__                                   | Positivity rate.                           | Number     |12.5%      | Labortests (not accessible); Falldetails (not accessible); (calculated) |


**Empty values**

| Value    | Meaning |
|----------| --------|
|zero      | Zero tests are reported.|
