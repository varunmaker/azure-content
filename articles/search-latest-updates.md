<properties 
	pageTitle="What’s new in the latest update to Azure Search" 
	description="Release notes for Azure Search describing the latest updates to the service" 
	services="search" 
	documentationCenter="" 
	authors="HeidiSteen" 
	manager="mblythe" 
	editor=""/>

<tags 
	ms.service="search" 
	ms.devlang="rest-api" 
	ms.workload="search" 
	ms.topic="article" 
	ms.tgt_pltfrm="na" 
	ms.date="03/05/2015" 
	ms.author="heidist"/>

#What’s new in the latest update to Azure Search#

Azure Search is now generally available, offering a 99.9% availability service-level agreement (SLA) for supported configurations of the [2015-02-28 version of the API](https://msdn.microsoft.com/en-us/library/azure/dn798935.aspx).

Watch this video for a demo and discussion of the latest features:

> [AZURE.VIDEO azure-search-general-availability-and-whats-new/]

##How features are versioned and rolled out##

Features are released through the [REST API](https://msdn.microsoft.com/en-us/library/azure/dn798935.aspx), [.NET SDK](http://go.microsoft.com/fwlink/?LinkId=528216), or both. This page lists and describes each release in terms of the functionality it provides.

Currently, only the REST APIs have multiple versions. Older APIs remain operational as we roll out new features. The only other release is the .NET SDK, which is in its first pre-release iteration. You can visit [Search service versioning](https://msdn.microsoft.com/en-us/library/azure/dn864560.aspx) to learn more about our versioning policy.

##.NET SDK 0.9.6-preview##
**Released: 2015 March 5**

Includes a client library, Microsoft.Azure.Search.dll, with two namespaces:

- [Microsoft.Azure.Search](https://msdn.microsoft.com/en-us/library/azure/microsoft.azure.search.aspx)
- [Microsoft.Azure.Search.Models](https://msdn.microsoft.com/en-us/library/azure/microsoft.azure.search.models.aspx)

Excludes:

- [Indexers](http://go.microsoft.com/fwlink/p/?LinkId=528173)
- [Management REST API](https://msdn.microsoft.com/en-us/library/azure/dn832684.aspx)
- [2015-02-28-Preview](http://azure.microsoft.com/en-us/documentation/articles/search-api-2015-02-28-Preview/) features (currently preview-only features consist of Microsoft natural language processors and `moreLikeThis`).

See [How to use Azure Search in .NET](http://go.microsoft.com/fwlink/p/?LinkId=528088) for guidance on installation and usage of the SDK.

##Api-version 2015-02-28-Preview##
**Released: 2015 March 5**

- [Microsoft natural language processors](http://azure.microsoft.com/en-us/documentation/articles/search-api-2015-02-28-Preview/) bring support for more languages and expansive stemming for all the languages supported by Office and Bing.

- [moreLikeThis=](http://azure.microsoft.com/en-us/documentation/articles/search-api-2015-02-28-Preview/) is a search parameter, mutually exclusive of `search=`, that triggers an alternate query execution path. Instead of full-text search of `search=` based on a search term input, `moreLikeThis=` finds documents that are similar to a given document by comparing their searchable fields.

##Api-version 2015-02-28##
**Released: 2015 March 5**

- [Indexers](http://go.microsoft.com/fwlink/p/?LinkID=528210) is a new feature that vastly simplifies indexing from data sources on Azure SQL Database, Azure DocumentDB, and SQL Server on Azure VMs.

- [Suggesters](https://msdn.microsoft.com/en-us/library/azure/dn798936.aspx) replaces the more limited, type-ahead query support of the previous implementation (it only matched on prefixes) by adding support for infix matching. This implementation can find matches anywhere in a term, and also supports fuzzy matching.

- [Tag boosting](http://go.microsoft.com/fwlink/p/?LinkId=528212) enables a new scenario for scoring profiles. In particular, it leverages persisted data (such as shopping preferences) so that you can boost search results for individual users, based on personalized information. 

See [Azure Search is now Generally Available](http://go.microsoft.com/fwlink/p/?LinkId=528211) for the service announcement on the Azure blog that discusses all of these features.

##Api-version 2014-10-20-Preview##
**Released: 2014 November, 2015 January**

- [Lucene language analyzers](http://azure.microsoft.com/en-us/documentation/articles/search-api-2014-10-20-preview/) was added to provide multi-lingual support for the custom language analyzers that are distributed with Lucene. 

- Tool support was introduced for building indexes, including scoring profiles, in the [Azure management portal](https://portal.azure.com).

##Api-version 2014-07-31-Preview##
**Released: 2014 August 21**

This release was the public preview for Azure Search, providing the following core features:

- REST API for index operations and document operations. The majority of the API is intact in 2015-02-28. You can access the documentation for this release at [Azure Search Service REST API Version 2014-07-31](http://azure.microsoft.com/en-us/documentation/articles/search-api-2014-07-31-preview/).

- Scoring profiles for tuning search results. A scoring profile adds criteria used to compute search scores. You can access the documentation for this release at [Azure Search Service Scoring Profiles REST API Version 2014-07-31](http://azure.microsoft.com/en-us/documentation/articles/search-api-scoring-profiles-2014-07-31-preview/).

- Geospatial support has been available from the beginning, provided through the `Edm.GeographyPoint` data type that has been part of Azure Search since its inception.

- Provisioning in the preview version of the [Azure management portal](https://portal.azure.com ). Azure Search was one of the few services that has only been available in the new portal.

##Management api-version 2015-02-28##
**Released: 2015 March 5**

[Management REST API](https://msdn.microsoft.com/en-us/library/azure/dn832684.aspx) marks the first release of the management API belonging to the generally available release of Azure Search. 

##Management api-version 2014-07-31-Preview##
**Released: 2014 October**

The preview release of [Management REST API](http://azure.microsoft.com/en-us/documentation/articles/search-management-api-2014-07-31-preview/) was added to support service administration programmatically. It is versioned independently of the service REST API.
