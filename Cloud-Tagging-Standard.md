# Tagging Standard for Cloud Projects

## Introduction

This document outlines the tagging standard that will be used to set meta data information associated with cloud projects in the Public Health Data Center of Excellence (PDCP). The tagging standard consists of mandatory and optional tags that must be filled out when creating a new subscription. The standard is designed to provide important information about the subscription, including the client organization, technical contacts, environment, data sensitivity, cloud usage profile, project name, and cost center.

## Mandatory and Optional Tags

The tagging standard consists of mandatory and optional tags that must be filled out when creating a new subscription. The following table lists the mandatory tags that must be filled out, along with their descriptions and example values:

| Tag Key           | Description                                                   | Examples        |
|-------------------|---------------------------------------------------------------|----------------|
| ClientOrganization| The department who is responsible for the subscription        | PHAC            |
| ProjectEmail      | The individual who is paying for the subscription             | johnsmith@canada.ca |
| TechnicalEmail    | The main technical contact(s) for the subscription             | jane.doe@canada.ca |
| Environment       | The type of environment                                        | sandbox, dev, test, QA, prod |
| DataSensitivity   | The highest data classification of the workloads in the subscription | Unclassified, Protected A, Protected B |
| CloudUsageProfile | The cloud usage profile for the workload                       | Profile 1, Profile 2, Profile 3, Profile 4, Profile 5 |
| ProjectName       | The name for the main workload or project in the subscription | Core Network |
| CostCenter        | (optional) The cost center used for charge back on the subscription costs | 555555 |



## Conclusion

The tagging standard outlined in this document is designed to ensure that all subscriptions managed by the PDCP contain important information about the client organization, technical contacts, environment, data sensitivity, cloud usage profile, project name, and cost center. By following this tagging standard,
