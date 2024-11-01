# API Experiences
API Experiences are the common everyday ways in which we experience APIs from both the producer and the consumer perspective, providing a set of common language that we use to describe how the humans involved with API operations experience things, including both business and technical stakeholders needs.

## API Commons
API Experiences are a new API Commons schema that is associated with API policies, which can then be bridged to API rules, helping translate very technical details into things that actually impact teams who are producing APIs as well as the consumers of APIs, focusing on optimizing and streamlining the experience over time.

## Example ([experience-example-1](experience-example-1.yml))

```
name: Change
slug: change
image: '/images/change.png'
description: Struggle with managing and communicating change across APIs across
  the lifecycle.
tags:
  - Change
  - Versioning
  - Versions
properties:
  - RoadMap
  - ChangeLog
  - Versioning 
```

## JSON Schema ([experience-json-schema](experience-json-schema.yml))

```
"$schema": http://json-schema.org/2020-12/schema
type: object
description: A schema to define the common experiences across API operations.
properties:
  name:
    type: string
    description: The name of the experience being defined.
  slug:
    type: string
    description: A slugified version of the experience name.
  image:
    type: string
    description: An image to represent the experience.
  description:
    type: string
    description: A more detailed version of the experience.
  tags:
    type: array
    description: The keywords and phrases applied to experience.
    items:
    - type: string
  properties:
    description: The APIs.json properties that apply to experience.
    type: array
    items:
    - type: string
required:
- name
- slug
- image
- description
- tags
- properties
```

# API Policies, Rules, Experience, and Guidance
Experiences are associated with policies, which then can also provide the bridge to the rules used to lint the business and technical contracts in place for APIs, helping filter and ground the governance of APIs in the things that will actually matter to both API producers and consumers when it comes making their jobs easier.

<img src="https://kinlane-productions2.s3.us-east-1.amazonaws.com/policies-rules-guidance-experience-lifecycle.jpg">

This work acknowledges that services, tooling, and the general approach of API governance is only using rules applied to OpenAPI, which is beginning to expand to AsyncAPI, GraphQL, and Arazzo workflows, but is proposing the first schema for aligning this work with business objectives, when teams are ready for it.

## Support
This work is in early stage of development and rapidly moving as they are being applied in a variety of user interfaces and approaches to the automation and reporting of API governance. If you would like to contribute, have any questions, or would like to inform the work happening, please submit a GitHub issue on the repository or email kin@apievangelist.com.