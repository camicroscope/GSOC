# caMicroscope GSoC 2023
<img src="https://avatars0.githubusercontent.com/u/12075069?s=200&v=4" width="150" height="150" align="left" style="padding:10px;"/> caMicroscope is a digital pathology image viewer with support for human/machine generated annotations and markups. The source code of the caMicroscope project can be found at https://github.com/camicroscope/caMicroscope, released with BSD 3-Clause License. In addition to the caMicroscope project, caMicroscope as an organization also hosts several related tools and products at https://github.com/camicroscope/

# Communicating with the mentors
We intend to use Slack as the primary medium of communication. The slack room at camicroscope.slack.com is used to discuss project ideas. You may join the caMicroscope Slack channel through our shared link - http://bit.ly/camicroscope

# Code Challenges
Code Challenges submissions should demonstrate creativity, understanding of the project, and ability to execute on a project proposal. Submit code challenges for early review and feedback here: [caMicroscope | GSOC 2023 | code challenge submission](https://forms.gle/moA6QwPZLMhuKJXD6) 
 
# List of Ideas
The following ideas were created with feedback from contributors and collaborators. Project ideas are not listed in any particular order. Submissions need not come from the below list, but should have reasonable relevance to the caMicroscope organization and its goals. Please feel free to discuss these or other project ideas on the email list or Slack group.  
** More ideas are upcoming **

***

## **[1] Machine Learning Assistant**

Many user actions in pathology data collection are mostly independent. Annotation, classification, and user review are produced largely by an expert opinion without use of machine learning tools. To augment this workflow, caMicroscope has added some specific tools which can assist with or validate annotations and classifications. However, at this time the tools are separate enough to often be practically slower than not using them.
This project, the Machine Learning Assistant, is to consider the needs of the user as well as the complexity to automatically and unobtrusively assist data collection by pathologists and other researchers. 
A significant amount of this project would be user experience focused, specifically finding ways to quickly provide insight using existing machine learning tools. To augment this, the project may include additional implementations, as well as runtime analysis to determine what information can be considered at a given time.

Difficulty: Hard
Project Length: Long

Primary Project Contact: Ryan Birmingham

Source Code: https://github.com/camicroscope/camicroscope 

Code Challenge: Create a frontend web application which uses tensorflow-js to provide some form of analysis on a user-supplied image unobtrusively. This should function on multiple timescales as possible, so that some information can be displayed immediately, while other slower-running calculations can be returned on completion.

## **[2] Dicom Support**

caMicroscope supports openslide compatible file types for its tiling engine. While many other formats are often requested to work without conversion, one of the most common suggestions that research groups and governmental organizations ask for is DICOM Whole Slide Imaging (See https://dicom.nema.org/dicom/dicomwsi/). This format follows the DICOM standards as are common in radiology, so this would help promote interdisciplinary research. This project would require creating an alternate tiling engine microservice which can efficiently serve regions of a slide from DICOM WSI format into either a simulated deepzoom image or the IIIF url pattern format (see https://iiif.io/).

Difficulty: Medium
Project Length: Short

Source Code: New Project. See https://github.com/camicroscope/iipimage for a similar project.

Primary Project Contact: Tony Pan

Code Challenge: Create a microservice in a language/framework of your choice which can serve metadata about any DICOM file.

## **[3] Multi-channel Imaging Support**

## **[4] Collection and Study Managment**

## **[5] Modularization of Components**

## **[6] Eaglescope Automatic Configuration**

Eaglescope is a web application for exploratory analysis on high dimensional datasets, especially biomedical datasets. This tool has been designed primarily to focus on cohort identification, that is to identify a set of criteria which produce distinct or interesting data. Right now, in order to create a dashboard, the entire layout needs to be specified in a configuration manifest. However, this has the side effect of requiring that users already understand the data well enough to select which possible visualizations would be most interesting.
This project, Eaglescope Automatic Configuration, aims to provide instant statistical insight into which fields or combinations of fields can be best represented in the various different visualizations implemented in eaglescope. This would have the added bonus of letting a user quickly explore a new dataset without writing any configuration. This has been proposed as a short project, and would focus on classical statistical methods. 

Difficulty: Difficult
Project Length: Short

Primary Project Contact: Ryan Birmingham

Source Code: https://github.com/sharmalab/eaglescope

Code Challenge: Create a web application which takes in a user-supplied file (e.g. csv) and uses SVD and/or dimensionality reduction to determine which feature(s) are most explanatory.


## **[7] Eaglescope/caMicroscope Integration**


&nbsp;
***
# Applying for GSOC

Mentors and evaluators usually look for:
* The proposal itself is clear relevant, and realistic.
* The contrubutor has demonstrated that they have the relevant skills to complete the proposal.
* The contrubutor has shown an interest in open source, especially caMicroscope. This includes community involvement.
* Code Challenges and other relevant demonstrations go above and beyond in some interesting way.

## Application Template

The following Template is provided to help organize all required information for a successful GSOC application. While following this template is not required, please be sure that your application is complete.

**1) Project Title:**

**2) Abstract / Project Summary**:

Summarize the project in your own words.

**3) Contributor Name:**

**4) Contributor Email and Slack username:**

**5) Potential Mentor(s):**

**6) Personal Background (Brief CV)**

**7) Project Goals**

(Enter as bullets)

..
     
..
     
..

**8) Detailed Project Proposal**

Describe what you propose to do for the project.

**9) Project Schedule**

Break the timeline into periods of approximately 7 days. Be clear if you have planned for a full-time or half-time project.

**10) Planned GSoC work hours**

Please indicate the work hours (including the timezone), that you hope to work on your project. 

**11) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Indicate any examinations or other personal commitments. 

**12) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).
