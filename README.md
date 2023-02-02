# caMicroscope GSoC 2023
<img src="https://avatars0.githubusercontent.com/u/12075069?s=200&v=4" width="150" height="150" align="left" style="padding:10px;"/> caMicroscope is a digital pathology image viewer with support for human/machine generated annotations and markups. The source code of the caMicroscope project can be found at https://github.com/camicroscope/caMicroscope, released with BSD 3-Clause License. In addition to the caMicroscope project, caMicroscope as an organization also hosts several related tools and products at https://github.com/camicroscope/

# Communicating with the mentors
We intend to use Slack as the primary medium of communication. The slack room at camicroscope.slack.com is used to discuss project ideas. You may join the caMicroscope Slack channel through our shared link - http://bit.ly/camicroscope

# Code Challenges
Code Challenges submissions should demonstrate creativity, understanding of the project, and ability to execute on a project proposal. Submit code challenges for early review and feedback here: [caMicroscope | GSOC 2023 | code challenge submission](https://forms.gle/moA6QwPZLMhuKJXD6) 
 
# List of Ideas
The following ideas were created with feedback from contributors and collaborators. Project ideas are not listed in any particular order. Submissions need not come from the below list, but should have reasonable relevance to the caMicroscope organization and its goals. Please feel free to discuss these or other project ideas on the email list or Slack group.  

***

## [1] Machine Learning Training Assistant

**Primary Mentors:** Tony Pan

**Overview** Many user actions in pathology data collection are mostly independent. Annotation, classification, and user review are produced largely by an expert opinion without use of machine learning tools. To augment this workflow, caMicroscope has added some specific tools which can assist with or validate annotations and classifications. However, at this time use of the tools usually require a pretrained model in order to use. There is a workflow for creating labeled dataset images and training in caMicroscope, but it is difficult to use in practice.
This project, the machine learning training assistant, would be both to consolidate and improve the user experience of the training workflow, as well as to find ways to improve performance and time taken for predictions.
This project would likely involve adding a microservice to allow training to run on a server or third party platform based upon configuration.
A significant amount of this project would be user experience focused, specifically finding ways to quickly provide insight using existing machine learning tools. To augment this, the project may include additional implementations, as well as runtime analysis to determine what information can be considered at a given time.

**Required Skill:** 

**Difficulty:** Hard

**Project Length:** Long

**Primary Project Contact:** Tony Pan

**Source Code**: https://github.com/camicroscope/camicroscope and https://github.com/camicroscope/caracal

**Code Challenge:** Create a frontend web application which uses tensorflow-js to provide some form of analysis on a user-supplied image unobtrusively. This should function on multiple timescales as possible, so that some information can be displayed immediately, while other slower-running calculations can be returned on completion.

## [2] Dicom Support

**Primary Mentors:** Tony Pan 

**Overview:** caMicroscope supports openslide compatible file types for its tiling engine. While many other formats are often requested to work without conversion, one of the most common suggestions that research groups and governmental organizations ask for is DICOM Whole Slide Imaging (See https://dicom.nema.org/dicom/dicomwsi/). This format follows the DICOM standards as are common in radiology, so this would help promote interdisciplinary research. This project would require creating an alternate tiling engine microservice which can efficiently serve regions of a slide from DICOM WSI format into either a simulated deepzoom image or the IIIF url pattern format (see https://iiif.io/).

**Required Skill:**

**Difficulty:** Medium

**Project Length:** Long

**Source Code:** New Project. See https://github.com/camicroscope/iipimage for a similar project.

**Primary Project Contact:** Tony Pan

**Code Challenge:** Create a microservice in a language/framework of your choice which can serve metadata about any DICOM file.

## [3] Multi-channel Imaging Support

**Primary Mentors:** Nan Li 

**Overview:** 

**Required Skill:** 

**Difficulty:** Medium 

**Project Length:** Long 

**Source Code:** 

**Primary Project Contact:** Nan Li

**Code Challenge:**

## [4] Collection and Study Management 

**Primary Mentors:** Nan Li 

**Overview:** caMicroscope is a widely used open-source end-to-end platform for digital pathology. It helps researchers and pathologists host, manage, and annotate the whole slide imaging (WSI). The WSIs and annotations are the most important fundamental dataset in caMicroscope. As the slides and annotations grows, researchers and pathologists need to an efficient way to organize slides and annotations. Currently, caMicroscope use the concept of collection to manage slides. Each annotation is directly associated with its slide. It is hard for researchers and pathologists to divide a study by using collection since the different studies need researchers and pathologists focus on. For example, some studies might focus on make annotations on a series of slides. And some studies might focus on evaluation on series of annotations. We propose an implementation intended for refactoring and extending current collection management. Design a novel collection and study management to help reorganize slides and annotations to help users organize their studies. 

**Required Skill:** Prior experience in Node.js, and mongoDB. Familiar with Javascript, HTML and CSS 

**Difficulty:** Medium 

**Project Length:** Long 

**Source Code:** https://github.com/camicroscope/caMicroscope and https://github.com/camicroscope/Caracal 

**Primary Project Contact:** Nan Li

**Code Challenge:** Use object-oriented design to create a simple webapp which provides the operation to manipulate the collection in MongoDB. The code challenge should focus on developing the backend in REST APIs which uses Node.js to operate mongoDB and a simple frontend to proof the contributors understanding the basic architecture of web application. 

## [5] Modularization of Components 

**Primary Mentors:** Nan Li 

Overview: caMicroscope is a web-based biomedical image and data viewer, with a strong emphasis on cancer pathology WSI (Whole Slide Imaging). Application is written in pure javascript, CSS and HTML and it makes developers and contributors easy to understand caMicroscope code base. However, the pure Javascript and CSS makes the code less regular and hard reuse by new features. It is increasing the development and maintenance problems. To keep caMicroscope become a robust and feasible application, the modularization design of frontend components should be involved. It will create a health and feasible fundamentals of caMicroscope development and maintenance. We propose to refactor and create a series of web components to help people who want to learn and use this project quickly creating a customized version to fit their demands.   

**Required Skill:** Prior experience in Javascript, HTML, CSS and Bootstrap. Understand object-oriented design (OOD) 

**Difficulty:** Medium 

**Project Length:** Long 

**Source Code:** https://github.com/camicroscope/caMicroscope 

**Primary Project Contact:** Nan Li

**Code Challenge:** A simple webapp demonstrating Web Components 

## [6] Eaglescope Automatic Configuration

**Primary Mentor:** Ryan Birmingham

**Overview:** Eaglescope is a web application for exploratory analysis on high dimensional datasets, especially biomedical datasets. This tool has been designed primarily to focus on cohort identification, that is to identify a set of criteria which produce distinct or interesting data. Right now, in order to create a dashboard, the entire layout needs to be specified in a configuration manifest. However, this has the side effect of requiring that users already understand the data well enough to select which possible visualizations would be most interesting.
This project, Eaglescope Automatic Configuration, aims to provide instant statistical insight into which fields or combinations of fields can be best represented in the various different visualizations implemented in eaglescope. This would have the added bonus of letting a user quickly explore a new dataset without writing any configuration. This has been proposed as a short project, and would focus on classical statistical methods. 

**Current Status:** New frontend application

**Required Skills:** UX, JavaScript, TensorFlow

**Difficulty:** Medium

**Project Length:** Short

**Source Code:** https://github.com/sharmalab/eaglescope

**Primary Project Contact:** Ryan Birmingham

**Code Challenge:** Use eaglescope to visualize a dataset in a selection of different ways.

## [7] User Driven Pathology Validation

**Primary Mentor:** Ryan Birmingham

**Overview:** caMicroscope has a viewer component and support for machine learning models. Thus, we have the components to build an alternate version of the viewer to host a pathologist vs machine learning model visual and numeric annotation comparison environment.
If the model is trusted, this application should function as a way for a human to test their observation skills in pathology. Alternatively, if a model is unvalidated, this would work as a way to test the model.  Practically, this would involve creating at least one interactive way to numerically compare a human input with a machine learning model classification or segmentation. Strong proposals would demonstrate at least a few such ways of showing this comparison both numerically and visually.
This would serve as a demo of caMicroscope, a way to validate machine learning models, and could be alternate kind of training exercise for pathologists.

**Current Status:** New frontend application

**Required Skills:** UX, JavaScript, TensorFlow

**Difficulty:** Hard

**Project Length:** Long

**Source Code:** https://github.com/camicroscope/camicroscope

**Primary Project Contact:** Ryan Birmingham

**Code Challenge:** Make a clone/minimum viable product of a game similar to geoguessr, focusing on the user interaction and scoring.

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
