# Tagging Standard for Cloud Projects

## Introduction

This document outlines the label standard that will be used to set meta data information associated with cloud projects in the Public Health Data Center of Excellence (PDCP). The tagging standard consists of tags that must be filled out when creating a new project. The standard is designed to provide important information about the project, including the client organization, technical contacts, environment, data sensitivity, cloud usage profile, and project name.

## Mandatory and Optional Tags

The tagging standard consists of mandatory and optional tags that must be filled out when creating a new subscription. The following table lists the mandatory tags that must be filled out, along with their descriptions and example values:

| Tag Key           | Description                                                   | Examples        |
|-------------------|---------------------------------------------------------------|----------------|
| clientorg         | The department who is responsible for the subscription        | PHAC            |
| projectlead       | The individual who is paying for the subscription             | john__dot__bain__at__phac-aspc__dot__gc__dot__ca |
| techlead          | The main technical contact(s) for the subscription             | john__dot__bain__at__phac-aspc__dot__gc__dot__ca |
| env               | The type of environment                                        | experiment, sandbox, dev, test, qa, prod |
| datasensitivity   | The highest data classification of the workloads in the subscription | unclass, proa, prob |
| cloudprofile      | The cloud usage profile for the workload                       | 1, 2, 3 |
| projectname       | The name for the main workload or project in the subscription | zero_sugar_zero_caffeine |

## Limitations
*Only hyphens (-), underscores (_), lowercase characters, and numbers are allowed. International characters are allowed.*

## Conclusion

The label standard outlined in this document is designed to ensure that all projects managed by the PDCP contain important information about the client organization, technical contacts, environment, data sensitivity, cloud usage profile, and project name.