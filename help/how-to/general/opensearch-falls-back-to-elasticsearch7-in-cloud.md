---
description: Short Description is a sentence stating that the article provides a solution for a certain problem; Followed with a call to action. Ideally, the size is 150-160 characters. Example: Learn how to solve an Adobe 
Analytics issue where you cannot see Server Call Usage. 
Check your permissions.
---

# Article Title

OpenSearch Search Engine Falls Back to Elasticsearch7 on Adobe Commerce Cloud (2.4.4, 2.4.5).

In Adobe Commerce versions 2.4.4 to 2.4.5 running on Cloud infrastructure, users may encounter an issue where configuring the OpenSearch search engine results in an unexpected fallback to Elasticsearch7. This behavior occurs despite OpenSearch being supported, and it is due to search engine restrictions specific to Cloud environments. This article explains the cause and provides a step-by-step solution to ensure search engine compatibility and stability in your deployment.

## Description:

Learn how to fix an issue in Adobe Commerce 2.4.4, 2.4.5 Cloud where setting the search engine to OpenSearch fails and falls back to Elasticsearch7.

### Environment

- Adobe Commerce 2.4.4, 2.4.5
- Adobe Commerce Cloud infrastructure

### Issue Description

When the search engine is configured to **OpenSearch**, the following error is logged in `var/log/support_report.log`.
Although OpenSearch is supported in these versions, the application still defaults to `elasticsearch7` on Cloud environments.

### Steps to Reproduce

1. Set `OpenSearch` as the search engine.
2. Deploy the code to Adobe Commerce Cloud 2.4.4 or 2.4.5.
3. Observe the fallback behavior in the log file.

## Resolution

To resolve this issue, update the `SEARCH_CONFIGURATION` environment variable in your `.magento.env.yaml` file to explicitly use `elasticsearch7`.
SEARCH_CONFIGURATION:```yaml
engine:elasticsearch7

### Cause

In Adobe Commerce 2.4.4 and 2.4.5, although OpenSearch is supported, **Cloud environments do not allow changing the search engine via the Admin panel**. The configuration is locked, and only elasticsearch7 is recognized until version 2.4.6, where OpenSearch support was fully integrated.

## Related Documentation

- [Cannot change search engine using Magento Admin Search engine menu is inaccessible](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/cannot-change-search-engine-using-magento-admin-search-engine-menu-is-inaccessible#adobe-commerce-on-cloud-infrastructure).
- [Locked fields in Magento Admin](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/locked-fields-in-magento-admin).
- [Search engine shown as Elasticsearch despite OpenSearch config](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/elasticsearch/search-engine-shown-elasticsearch-despite-open-search).
