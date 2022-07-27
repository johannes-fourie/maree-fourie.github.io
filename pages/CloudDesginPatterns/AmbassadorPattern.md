---
layout: page
title: "Ambassador pattern"
permalink: /CloudDesginPatterns/
---

The ambassador service sends network requests on behalf of the application services. It acts as an out-of-process proxy that is co-located with the client.

**Offload connectivity tasks**
: $\rightarrow$ Offload common client connectivity tasks such as <u>monitoring</u>, <u>logging</u>, <u>routing</u>, <u>security</u> (such as TLS), and <u>resiliency patterns</u> in a language agnostic way.
: $\rightarrow$ Extend the networking functionality of legacy apps or difficult to modify apps.
: $\rightarrow$ Enable specialized teams to implement connectivity features.

![](/pages/CloudDesginPatterns/img/Ambassador/AmbassadorPattern.svg)

## Example

We have an application that makes calls to a remote service via and ambassador. The ambassador has retry logic.

![](/pages/CloudDesginPatterns/img/Ambassador/Application.svg)

![](/pages/CloudDesginPatterns/img/Ambassador/Ambassador.svg)

![](/pages/CloudDesginPatterns/img/Ambassador/RemoteService.svg)

We want to verify that the Ambassador will not add to much latency to our system.

The Ambassador has retry logic.

## References
- [Ambassador pattern, Microsoft Docs](https://docs.microsoft.com/en-us/azure/architecture/patterns/ambassador)
