# Public Health Data Center of Practice Unique Project ID System

## Overview
The Public Health Data Center of Practice has implemented a unique project ID system to help manage and organize our key projects. This system is based on a consistent format that allows us to easily categorize and filter projects based on their purpose, status, and other relevant factors.

## How it Works
Rules:
 * all lower case
 * expressed as pseudo-regex:
	* ph(d|t|p|x|o)-(a|b|s|i)-#-nametextnospaces
	* ph = public health
	* (d|t|p|x|o) THIS IS ONLY REQUIRED AT PROJECT LEVEL; DEFAULT TO ‘O’ IF ONLY 1 ENV
		 * d = dev
		* t = test
		* p = prod
		* x = experimental
		* o = other
	* (a|b|s|i)
		 * a = automated intake (simplest)
		 * b = more complex via DST board
		 * s = internal services
		 * i = internal project
		 * \# = incrementing number with no padding (i.e. '1' not '0001')
 * examples:
	 * folder: ph-s-3-fldrprojectconf 
		 * project: pho-s-3-fldrprojectconf
	 * folder: ph-b-1234-diseaseprofiler 
		 * project: phd-b-1234-diseaseprofiler
		 * project: pht-b-1234-diseaseprofiler 
		 * project: php-b-1234-diseaseprofiler 
	 * folder: ph-b-223-vaccinestudy project:    
		 * pho-b-223-vaccinestudy

Project names have a 30-character limit which may mean truncation of the right side if the name is too long. Additional values will be added via metadata (business contact, technical contact, business intake id, etc.)

## Benefits
Our unique project ID system provides several benefits:

- Consistent format: By following a consistent format for all project IDs, we can easily recognize and categorize projects based on their ID.
- Easy filtering: Our project ID system allows us to filter projects based on their ID, which can help us quickly find and organize projects based on their category, status, or other relevant factors.
- Scalability: By assigning a unique ID to each project, we can easily add new projects to the list and ensure that they are properly categorized and organized.

## Conclusion
The unique project ID system implemented by the Public Health Data Center of Practice helps us manage and organize our key projects in a way that is consistent, scalable, and easy to navigate. By using this system, we can ensure that our projects are properly categorized and organized, which ultimately helps us achieve our goal of improving public health outcomes through the collection, analysis, and sharing of health data.
