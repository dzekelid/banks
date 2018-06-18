---
name: Open FinTech
x-slug: open-fintech
description: International standards yield technological, economic and social advantages.
  Standards speed up the development of new applications and simplify the process
  of communication between the services. Data and service is available under the Open
  Database License (ODbL). It is an open standard and open data, every player of FinTech
  market can contribute to development and enhancement. All data is available through
  Rest API based on JSON API standard.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/open-fintech-io.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Banks
created: "2018-06-17"
modified: "2018-06-17"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/banks/master/_listings/open-fintech/apis.md
specificationVersion: "0.14"
apis:
- name: Open FinTech List of banks
  x-api-slug: open-fintech
  description: Returns list of banks. Each object contains general information about
    bank such as name and status, also information about bank details and related
    link to main organization.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/open-fintech-io.png
  humanURL: http://openfintech.io
  baseURL: https://api.openfintech.io//v1///banks
  tags: Banks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/banks/master/_listings/open-fintech/banks-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/banks/master/_listings/open-fintech/banks-get-openapi.md
- name: Open FinTech Bank by ID
  x-api-slug: open-fintech
  description: Returns bank with specific ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/open-fintech-io.png
  humanURL: http://openfintech.io
  baseURL: https://api.openfintech.io//v1///banks/{id}
  tags: Banks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/banks/master/_listings/open-fintech/banksid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/banks/master/_listings/open-fintech/banksid-get-openapi.md
- name: Open FinTech
  x-api-slug: open-fintech
  description: International standards yield technological, economic and social advantages.
    Standards speed up the development of new applications and simplify the process
    of communication between the services. Data and service is available under the
    Open Database License (ODbL). It is an open standard and open data, every player
    of FinTech market can contribute to development and enhancement. All data is available
    through Rest API based on JSON API standard.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/open-fintech-io.png
  humanURL: http://openfintech.io
  baseURL: https://api.openfintech.io//v1/
  tags: Banks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/banks/master/_listings/open-fintech/openapi.md
x-common:
- type: x-developer
  url: https://docs.openfintech.io/
- type: x-getting-started
  url: https://docs.openfintech.io/#section/Get-Started
- type: x-github
  url: https://github.com/openfintechio
- type: x-website
  url: http://openfintech.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---