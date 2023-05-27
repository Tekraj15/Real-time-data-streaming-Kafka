# Real-time-data_streaming-Kafka


Ingest clickstream data from Kafka.
Store the ingested data in data store of your choice, with the following schema:
Row key: Unique identifier for each click event.
Column families:
click_data: Contains columns for the user ID, timestamp, and URL of the clicked page.
geo_data: Contains columns for the user's country and city, as determined by their IP address.
user_agent_data: Contains columns for the user's browser, operating system, and device, as determined by their
user agent string.
Periodically process the stored clickstream data in any data store by aggregating the data by URL and country, and
calculating the number of clicks, unique users, and average time spent on each URL by users from each country.
Index the processed data in Elasticsearch.
