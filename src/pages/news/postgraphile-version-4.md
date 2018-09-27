---
layout: page
path: /news/postgraphile-version-4/
title: PostGraphile Version 4 is released
---

## PostGraphile Launches Version 4

**The original GraphQL API for PostgreSQL: now vastly more performant, customisable and extensible than ever before**

After a year of development and testing, Benjie Gillam is pleased to announce the release of PostGraphile version 4 - the most customisable and extensible automatic GraphQL API for PostgreSQL yet. PostGraphile - previously known as PostGraphQL - has been re-written from the ground up with a strong focus on performance, best practices and flexibility. This has been enabled through the creation of Graphile Engine - a powerful datasource-agnostic GraphQL Engine that has extensibility and performance at its core - upon which PostGraphile Version 4 is built.

PostGraphile exposes the powerful next generation features of PostgreSQL, enabling developers to use their existing Postgres knowledge to build a secure and highly performant GraphQL API with just one command line. PostGraphile encourages developers to embrace the powerful features of Postgres, the most advanced open source database, rather than trust and learn a new set of tools and interfaces.

* **PostGraphile Version 4 is highly performant**

Benjie has rebuilt the core of PostGraphile entirely, with a strong focus on performance. Unlike other solutions, PostGraphile is able to look at the GraphQL query holistically and find the most efficient way of executing it. This has lead to a large increase in the request throughput, and a 94% decrease in latency. Peak memory usage has also reduced by 92% as compared to Version 3. The result is a much faster applications, and happier users - especially those on mobile. PostGraphile v3 users will be able to reap these massive performance improvements simply by updating - no need to change their application code.

<div class="flex flex-row flex-wrap">
<div class='text-center col-xs-12 col-md-3 col-lg-5 postgraphile-graphs-requests-per-second'></div>
<div class='text-center col-xs-12 col-md-3 col-lg-5 postgraphile-graphs-average-latency-label'></div>
</div>

[Read more about the stunning new performance of PostGraphile version 4](/postgraphile/performance/)

* **Version 4 is highly customisable**

Beyond the plugin interface, Version 4 has added three new features to help developers streamline their GraphQL schema. First, unnecessary functionality from PostgreSQL extensions is now filtered out by default, meaning only the tables and functions the developer has added are exposed. Secondly, PostGraphile can now inspect the database permissions, and automatically removes types and fields from the generated schema that the user has no way of accessing. Finally, version 4 introduces the concept of "smart comments".

The new smart comments functionality enables the developer to customise their GraphQL schema as they see fit. By adding smart comments, the developer can easily perform operations such as renaming fields without modifying the underlying table structure. Besides renaming fields, current operations include renaming types, detailing when a field should be included or not (e.g. making a field read-only), and handling deprecation gracefully. Plugin authors are already using the smart comments functionality to add new features to their PostGraphile schemas, such as adding relations on views.

These features lead to smaller GraphQL schemas that are easier for developers to understand and manage without sacrificing desired functionality.

[Read more about the new smart comments system](/postgraphile/smart-comments/)

* **Version 4 is highly extensible**

Before commencing work on PostGraphile Version 4, Benjie reviewed every issue in the PostGraphile bug tracker, and concluded that a rigid one-size-fits all GraphQL API was too restrictive for many users. The rigid nature of v3 resulted in a number of users having to compromise with workarounds such as schema stitching, or resort to maintaining a separate fork of the project to add their desired functionality. With this in mind Benjie set out to find a solution to all these issues.

PostGraphile became a modular project, with its GraphQL generation powered by a new plugin-based project named Graphile Engine. Users can now use plugins to add functionality to their GraphQL schema without requiring modifications to the core - and they can even share these features with the world. During the development stages of Graphile Engine, a community of plugin writers formed; with their help, the plugin system solidified into the capable production-ready system that Benjie is proud to be releasing today. This work has negated the need to maintain forks of PostGraphile, and has lead to a growing ecosystem of functionality putting PostGraphile at the forefront of PostgreSQL GraphQL APIs.

[Read more about the new plug in system](/postgraphile/extending/)

**PostGraphile is open source, supported by the community**

This release of PostGraphile wouldn’t have been possible without the community. Benjie says, “The community's response to PostGraphile has been amazing! People have found so many ways to help support the project: from testing and reporting issues, to documentation fixes, and even large feature development. Their sponsorship now funds one day a week dedicated to PostGraphile development, and this support is growing every month which is already leading to more features and faster releases. This voluntary financial support from the community is very motivational, a great antidote to the burn-out that's common in open source maintainers, and it's exciting to be turning PostGraphile into a sustainable open source project that people can rely on for years to come. It's also wonderful to see the community being so supportive of each other - sharing knowledge, debugging issues, testing and sharing plugins. There's so much more to come from PostGraphile - bring on the future!”