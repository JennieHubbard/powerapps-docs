---
title: What is Common Data Service for Apps? | Microsoft Docs
description: Introduction to Common Data Service for Apps, entities, and server-side logic.
documentationcenter: na
author: clwesene
manager: kfile
editor: ''
tags: ''

ms.service: powerapps
ms.devlang: na
ms.topic: conceptual
ms.component: cds
ms.date: 3/21/2018
ms.author: clwesene

---
# What is Common Data Service for Apps?

Common Data Service for Apps allows you to securely store and manage data that's used in apps you've developed or apps from Microsoft and app providers. Data within CDS for Apps is stored within a set of standard and custom entities. An entity is a set of fields used to store data similarly to a table within a database. After your data is stored you can use Microsoft PowerApps to build rich applications using your data:

* Leverage existing standard entities or create custom entities to support your scenario and application.
* Create PowerApps and Flows directly against CDS for Apps.
* Add custom fields, and relationships to standard entities where additional information is needed.
* Create calculated and roll up fields to your entities to provide consistent calculations across apps and analytics.
* Define business rules to ensure data quality within entities, regardless of the which app is accessing or editing your data.
* Create workflows and leverage integration with Microsoft Flow to drive additional actions and business processes against your data.
* Incorporate standard and custom entities into an app that you're developing as easily as you would with data in other sources.
* Connect to your data from Microsoft Excel using CDS for Apps productivity add-ins.
* Easily import and synchronize your data using Power Query.
* Secure your data within your organization using role-based security against standard and custom entities.
* Provide global support for your data and applications by leveraging translation of entity and field names in your user's language.

Each entity contains a set of records that users can create, read, update, and delete depending on their permissions. You can create relationships between entities so that you can look up information in one entity based on a record in another entity. For example, you could create a custom entity to track events which a customer had attended. By adding the Customer to your custom entity as a lookup field, you establish a relationship between the two entities which can be leveraged in your app and in reporting.

For information on purchasing a plan for using CDS for Apps, see [Pricing info](../../administrator/pricing-billing-skus.md).

## Why use Common Data Service for Apps?
Entities within CDS for Apps, both standard and custom, allow a secure and cloud-based storage option for your data. Entities allow you to create a business-focused definition of your data for use within your apps. If you're not sure if entities are your best option, consider these benefits:

* **Easy to manage** - Both the metadata and data are stored in the cloud. You don't need to worry about the details of how they're stored.
* **Easy to share** - You can easily share data with your colleagues because PowerApps manages the permissions.
* **Easy to secure** - Data is securely stored so that users can see it only if you grant them access. Role-based security allows you to control access to entities for different users within your organization.
* **Rich metadata** - Data types and relationships are leveraged directly within PowerApps. For example, defining a field type URL will present your data as a hyperlink within your app.
* **Logic and validation** - Define calculated fields, business rules, workflows and business process flows to ensure the data quality and drive business processes.
* **Productivity tools** - Entities are available within the add-ins for Microsoft Excel to increase productivity, and ensure your data is accessible.

When you develop an app, you can use standard entities, custom entities, or both. If a standard entity can serve a particular purpose in your app, you should use it rather than developing a custom entity that does the same thing. If a standard entity would serve a purpose with a few changes, you can add fields to suit your needs.

* CDS for Apps provides standard entities by default. These are designed, in accordance with best practices, to capture the most common concepts for an organization, such as Contacts, Accounts, and Products. For a full list of entities, see [Standard entities](data-platform-intro.md#standard-entities).
* You can extend the functionality of standard entities by creating one or more custom entities to store information that's unique to your organization. For more information, see [How to create a custom entity](create-custom-entity.md).

> [!NOTE]
> If possible, use standard entities (with custom fields added, if required). This will ensure that you can benefit from new features or apps that leverage these entities in the future.

## Interacting with entities

When using a standard entity or creating a custom entity there are multiple elements available within each one and different actions that can be performed. Depending on how simple or advanced your business scenario is will determine which features you will need to use. To see the entities available within your environment, sign in to [PowerApps](https://web.powerapps.com), and click Data and then Entities from the left menu.

![Entity Details](./media/data-platform-cds-intro/entitylist.png "Entity Details")

* Each **field** allows you to define a piece of information to be collected, and the data type or format you would like to display it. Fields are similar to columns in databases or Excel.
* Alternate **keys** allow efficient and accurate search and interaction with records in the entity when not using the standard unique identifier. This is important when using a Business Key or integrating with an external system.
* Each entity can have multiple **relationships** to other entities to support look ups and queries across entities. Relationships can create to support Many-to-one, One-to-many and Many-to-many relationships.
* **Views** allow each entity can be presented in multiple ways, including which fields are displayed, filtering and sorting of the data. These presentations are saved as views and can be consumed in different apps, for example you may only want to see Active Accounts within your app so you would use a view which is pre filtered to only show Active accounts to avoid repeating the filter in each consuming app.
* **Business rules**  can be used to validate data being created and updated in entities to ensure data quality. Each business rule can validate data across multiple fields and entities, prompt warning and error messages regardless of the app being used to create the data.
* **Data** stored within CDS for Apps is available through the PowerApps portal, PowerApps, Microsoft Excel and Web APIs for Developers.

### System fields
All entities, whether standard or custom, are created with a set of read-only fields that you can't change, delete, or set to a value. These are the most important system fields:

## Logic and validation

Entities within CDS for Apps can leverage rich server-side logic and validation to ensure data quality and reduce repetitive code in each app creating and using data in the entity.

* **Business rules** can validate data across multiple fields and entities, prompt warning and error messages regardless of the app being used to create the data. For more information, see [Create a business rule](./data-platform-create-business-rule.md).
* **Business process flows** guide users to ensure data is entered consistently and follow the same steps every time. Business process flows are currently only supported for Model driven apps. For more information, see [Business process flows overview](/dynamics365/customer-engagement/customize/business-process-flows-overview).
* **Workflows** allow you to automate business processes without a user interaction. For more information, see [Workflows overview](/dynamics365/customer-engagement/customize/workflow-processes).
* **Business logic with code** supports more advanced developer scenarios to extend the application directly through code. For more information, see [Apply business logic with code](../../developer/common-data-service/apply-business-logic-with-code.md).

## Getting Data into Common Data Service for Apps

There are several ways to start getting data into CDS for Apps:

* Create a PowerApp or Flow to start creating data.
* Use Power Query to connect to an online or on-premise data source and import it directly into CDS for Apps. Power Query also allows you to create the entities during import based off the schema of your source as well as perform transformations to your data during import. For more information, see [Add data to an entity in Common Data Service for Apps by using Power Query](./data-platform-cds-newentity-pq.md).

## Developer Capabilities

In addition to the features available through the [PowerApps](https://web.powerapps.com) portal, CDS for Apps also includes features for developers to programmatically access metadata and data to create entities and business logic, as well as interact with data. For more information, see [Common Data Service for Apps Developer Overview](../../developer/common-data-service/overview.md)

## Get started
Try it out by creating an app using a standard entity or [create a custom entity](create-custom-entity.md), and then [create an app that uses that entity](../canvas-apps/data-platform-create-app.md).

## Privacy notice
With the Microsoft PowerApps common data model we collect and store custom entity and field names in our diagnostic systems.  We use this knowledge to improve the common data model for our customers. The entity and field names that Creators create help us understand scenarios that are common across the Microsoft PowerApps community and ascertain gaps in the service’s standard entity coverage, such as schemas related to organizations. The data in the database tables associated with these entities is not accessed or used by Microsoft or replicated outside of the region in which the database is provisioned. Note, however, the custom entity and field names may be replicated across regions and are deleted in accordance with our data retention policies. Microsoft is committed to your privacy as described further in our [Trust Center](https://www.microsoft.com/trustcenter/Privacy/default.aspx).
