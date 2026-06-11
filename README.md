# Email-Marketing-Analytics-SQL
## Business Need
The objective is to analyze account creation dynamics, monitor email interaction funnels (Sends, Opens, Clicks), and evaluate user behavior across dimensions such as send intervals, account verification, and subscription status. This data enables cross-country performance comparisons, identification of high-value markets, and precise user segmentation for targeted CRM campaigns.

## Developed Solution
Engineered an optimized data pipeline in Google BigQuery that unifies disparate account and communication logs into a single, comprehensive analytical layer. The solution utilizes advanced CTEs and window functions to ranks core markets without data duplication.

### List of output categorical values (Dimensions)
* **date** — Baseline date (Account creation date for user metrics; Email timestamp for messaging metrics).
* **country** — User's geographic location.
* **send_interval** — Account-defined messaging frequency preference.
* **is_verified** — Account verification status (True/False).
* **is_unsubscribed** — User subscription state (True/False).

### List of key metrics
* **account_cnt** — Total volume of newly registered accounts.
* **sent_msg** — Number of outbound messages dispatched.
* **open_msg** — Number of messages opened by users.
* **visit_msg** — Number of click-throughs (website visits) generated from emails.

### List of additional metrics
* **total_country_account_cnt** — Cumulative subscriber base per country.
* **total_country_sent_cnt** — Cumulative message volume per country.
* **rank_total_country_account_cnt** — Country ranking based on user acquisition scale.
* **rank_total_country_sent_cnt** — Country ranking based on communication density.

### Result of code execution
