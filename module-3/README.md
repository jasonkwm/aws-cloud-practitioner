# Table of Content
- [AWS Global Infrastructure](#aws-global-infrastructure)
  - [Selecting a Region](#selecting-a-region)
  - [Availability Zones](#availability-zones)
- [Edge Locations](#edge-locations-cdn)
- 
 
## AWS Global Infrastructure

### Selecting a Region
When determining the right Region for your services, data, and applications, consider the following four business factors.

- Compliance with data governance and legal requirements
  - Location-specific data regulations
- Proximity to your customers
  - Faster content delivery to customers
- Available services within a Region
  - Region might not have all the features that you want to offer to customers
- Pricing
  - Cost of services can vary from Region to Region.

### Availability Zones
- A single data center or a `group` of data centers within a Region
- Availability Zones are located `tens of miles apart` from each other
- Close enough to have `low latency` between Availability Zones
- Distant enough to reduce the chance of a disaster affecting multiple Availability Zones.
### Edge Locations (CDN)
Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery.
