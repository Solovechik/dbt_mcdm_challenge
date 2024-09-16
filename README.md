# Marketing common data modelling challenge
Welcome to Marketing common data modelling challenge!


## Task
At Improvado, we use marketing common data models (MCDM) to map data from various ad platforms into a single one. MCDM can help marketers with questions like: "Where clicks better on Facebook or Tiktok?"

Imagine that MCDM behind dashboard is lost somehow. You need to rebuilt it.
You have:
* raw data from the ad systems (seeds folder)
* the MCDM table structure for this report
* and the [dashboard](https://lookerstudio.google.com/reporting/fa668749-b82f-41a8-a12e-f7d9c0733b57/page/tEnnC)

In this situation, we've got checklist that you can follow (or not):
* begin a new dbt project locally, utilizing Clickhouse as the DWH (using Docker or not is up to you)
* use the raw data from the ad platforms and the MCDM table structure
* re-create models for the **ads_basic_performance** report


### How to Submit
Please provide an answer in the [typeform](https://improvado.typeform.com/to/efqlu4kP). 
Your GitHub repository must contain: 
* a completed dbt project for the **ads_basic_performance** report
* a set of commands to re-create a MCDM
* csv file for every chart in the example [dashboard](https://lookerstudio.google.com/reporting/fa668749-b82f-41a8-a12e-f7d9c0733b57/page/tEnnC)
* a brief set of instructions (in md file in your repo) for adding data from new ad platforms into your MCDM
* docker-compose.yml which runs all models and outputs their results as 4 separate tables into CLI (optionally)


### Hints
- **Cost per engage** is just a spended sum divided by sum of engagements
- **Conversion cost** is calculated by dividing sum of spended by total conversions count
- **Impressions by channel** is a sum of impressions for each channel
- **CPC** gets like sum of spended divided by clicks count


### Tools
To complete this task, you will need the following tools:
-   dbt-core
-   Clickhouse
-   Docker (optionally)


### Tool Instructions
To help you get started, here are some resources on how to use the necessary tools:
* [dbt Fundamentals](https://courses.getdbt.com/courses/fundamentals). Relevant chapters include:
	* Setting up dbt Cloud (17 minutes)
	* Models and Sources (40 minutes)


### Additional Resources
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- [Short overview](https://improvado.io/products/mcdm) for Improvado MCDM


### How to Use the Repository
The repository contains raw data from various ad platforms, as well as the MCDM structure for the **ads_basic_performance** report, which are provided as seeds:

-   src_ads_bing_all_data
-   src_ads_creative_facebook_all_data
-   src_ads_tiktok_ads_all_data
-   src_promoted_tweets_twitter_all_data
-   mcdm_paid_ads_basic_performance_structure

You need to create a new dbt project and find a use for the given files.


### Q&A
	Q: How to validate results for my model? 
	A: Compare your dashboard with the dashboard from task. If some numbers doesn't match, then some fiels in your model got incorrect mapped  

	Q: What if there're no MCDM sctructure field in raw datasource data?
	A: So you started understending the main goal of this task :-)	Suggest wich field or fields corresponds to MCDM ones by their meaning. If there're no such fields, then probably datasource just doesnt got them
