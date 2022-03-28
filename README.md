# Scrape Oryx
## About
This is a repo for the latest datasets scraped from Oryx' excellent post detailing materiel lost by all sides in the [Russian invasion of Ukraine](https://www.oryxspioenkop.com/2022/02/attack-on-europe-documenting-equipment.html).

### Datasets

#### daily_count.csv

Daily Count provides a running tally of equipment losses by type.

| Variable        | Variable Type | Description                                                     |
|-----------------|---------------|-----------------------------------------------------------------|
| country         | character     | The country to whom the materiel belongs.                       |
| equipment_type  | character     | The type of materiel.                                           |
| destroyed       | numeric       | A count of destroyed materiel                                   |
| abandoned       | numeric       | A count of abandoned materiel                                   |
| captured        | numeric       | A count of captured materiel                                    |
| damaged         | numeric       | A count of damaged materiel                                     |
| type_total      | numeric       | A count of materiel across all categories                       |
| date_recorded   | date          | Date the count was recorded stored as YYYY-MM-DD                |
| destroyed_diff  | numeric       | A number showing the differences in count from the previous day |
| abandoned_diff  | numeric       | A number showing the differences in count from the previous day |
| captured_diff   | numeric       | A number showing the differences in count from the previous day |
| damaged_diff    | numeric       | A number showing the differences in count from the previous day |
| type_total_diff | numeric       | A number showing the differences in count from the previous day |

#### total_by_system.csv

This dataset includes one row for each unique observation scraped from the website. A unique row is defined as a unique combination of `country`, `origin`, `system`, `status`, `url`.

| Variable      | Variable Type | Description                                                                                                          |
|---------------|---------------|----------------------------------------------------------------------------------------------------------------------|
| country       | character     | The country to whom the materiel belongs                                                                             |
| origin        | character     | The country of the systems origination / manufacture                                                                 |
| system        | character     | The weapon system                                                                                                    |
| status        | character     | The status of the system. Valid values are: destroyed, abandoned, damaged, or captured                               |
| url           | character     | A url to the image used to verify the status of the equipment                                                        |
| date_recorded | date          | Date the count was recorded stored as YYYY-MM-DD                                                                     |
