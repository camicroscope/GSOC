# caMicroscope GSoC 2021
<img src="https://avatars0.githubusercontent.com/u/12075069?s=200&v=4" width="150" height="150" align="left" style="padding:10px;"/> caMicroscope is a digital pathology image viewer with support for human/machine generated annotations and markups. The source code of the caMicroscope project can be found at https://github.com/camicroscope/caMicroscope, released with BSD 3-Clause License. In addition to the caMicroscope project, caMicroscope as an organization also hosts several related tools and products at https://github.com/camicroscope/

For 2021, the scope of GSOC projects have changed. Since the projects will be shorter, the camicroscope community will be able to focus on smaller interesting projects. We look forward to sharing our thoughts going forward, and thank you for your patience.

# Communicating with the mentors
We intend to use Slack as the primary medium of communication. The slack room at camicroscope.slack.com is used to discuss project ideas. You may join the caMicroscope Slack channel through our shared link - http://bit.ly/camicroscope

# Code Challenges
Code Challenges demonstrate a student's creativity, understanding of the project, and ability to execute on a project proposal. Submit code challenges for early review and feedback here: [caMicroscope | GSOC 2021 | code challenge submission](https://forms.gle/k4ZcH75UYG4y2tRJ7) 
 
# List of Ideas
The following ideas were created with feedback from contributors and collaborators. Submissions need not come from the below list, but should have reasonable relevance to the caMicroscope organization and its goals. Please feel free to discuss these or other project ideas on the email list or Slack group.  
** More ideas are upcoming **

***

**[1] Real-time Collaborative Pathology**

**Primary Mentor:**  Akhil Rana

**Overview:** 

A fundamental use case of caMicroscope is collaboration between different pathologists. This has been done in steps, where one scientist annotates and image, then shares a reference to their work for validation. However, it can be useful to work together in real time on a single slide to assist with training and research. This kind of fast collaboration is traditionally done by having different people share a screen, but this is made more difficult as remote work becomes more prevalant. To this end, we propose use of a simple server to relay events from users to each other. This project would involve some amount of decisions and design of relevant UX added to accomplish this.

**Current Status:** Deep hibernation: earlier beta/proof of concepts left over from years ago.

**Required Skills:** Websockets (or similar), JavaScript, OpenSeadragon, 

**Code Challenge:** A simple text chat app using websockets or a similar protocol.

**Source Code:** https://github.com/caMicroscope/caMicroscope 

***

**[2] Pathology Smartpens**

**Primary Mentor:**  Insiyah Hajoori and/or Nan Li

**Overview:** 

This project would involve adapting pathology annotation tools to prefer following edges in the base image when close. This task could be implemented using machine learning, computer vision, or a mix of the two. In order to use the tool effectively, this would involve expanding the user functions surrounding annotation, such as moving points in the drawing. Specific UI flow is up to the implementer; perhaps it's more useful to leave drawings alone, but have a button which snaps drawings to the nearest edge when pushed.

**Current Status:** The current annotation tools perform point simplification after a user finishes drawing without any consideration of the base image.

**Required Skills:** JavaScript, tensorFlow.js, computer vision

**Code Challenge:** Create a page or tool which performs edge detection on a given image and, given a point, returns the distance from that point to the closest edge.

**Source Code:** https://github.com/caMicroscope/caMicroscope

***

**[3] Cross-Slide Coordinated Viewing**

**Primary Mentor:**  Nan Li

**Overview:** 

Often, it's useful for users to compare different results on an image. To facilitate this, caMicrocope supports viewing the same image with different results, such as heatmaps, segmentations, and annotations, in a coordinated fashion. Since adjacent tissue slice images are usually quite similar, it can be useful to have a similar coordination between different images.
This project focuses on creating a tool to allow a user to do this. The two different tissue samples may be differently situated in their images, and may require a user to change scale, position, and rotation to sync up the two images.

**Current Status:** The current coordinated view tools are used for different results on the same image, with no support for multiple images at once.

**Required Skills:** JavaScript, OpenSeadragon

**Code Challenge:** Link user interaction across two OpenSeadragon instances if a checkbox is checked, otherwise, let them move independently.

**Source Code:** https://github.com/caMicroscope/caMicroscope 

***

**[4] Data Product User Experience**

**Primary Mentor:**  Ryan Birmingham

**Overview:** 

Currently, the main paradigm of caMicroscope is the slide. However, some scientists are more interested in other kinds of data products, such as annotations, heatmaps, patches, and so on. As a result, we aim to make loading and downloading these results easier. This project would involve a batch loader for results of different kinds so that working with these results is as painless as possible to the user.

**Current Status:** UI for slides exists, but can be expanded to other datatypes. Loaders exist for other datatypes as scripts.

**Required Skills:** UX design, JavaScript, HTML

**Code Challenge:** Create a demo table which toggles grouping of data by a particular field.

**Source Code:** https://github.com/caMicroscope/caMicroscope

***

**[5] Role Based Authentication**

**Primary Mentor:**  Ryan Birmingham and/or Erich Bremer

**Overview:** 

Currently, caMicroscope has a attribute based access control system for slides, which we describe as "filters". However, this does not map cleanly onto the way that users conceptualize authentication. Instead, we propose role based authentication on not only slides, but on all data products. A primary concern would be to minimize or eliminate any performance hit associated with adding this feature.

**Current Status:** New Feature of existing backend server.

**Required Skills:** JavaScript, Security

**Code Challenge:** Make a simple API which returns a list of items using RBAC to only return ones a particular user is allowed to see. For simplicity, we recommend using a url parameter to identify a user without worrying about security for this challenge.

**Source Code:** https://github.com/caMicroscope/caracal

***

**[6] Caching Slow DB Results on Backend**

**Primary Mentor:**  Ryan Birmingham

**Overview:** 

Some operations performed on the mongo database are slow, especially collecting distinct forms of metadata given a collection of results. Since new forms of results aren't introduced particularly often, it may be useful to allow the application to run an API call against cached results first, before making the slower call. Note specifically that the list of annotation layers has taken on the order of 10 seconds if a large number of segmentations are loaded, so this would have an appreciable impact on app performance.

**Current Status:** New Feature of existing backend server.

**Required Skills:** JavaScript, Caching

**Code Challenge:** Make a simple API which caches its results without using cache calls from an existing library.

**Source Code:** https://github.com/caMicroscope/caracal

***

**[7] Modularize the current code base for quick and easy workflow / task customization - Collaboration with FDA**

**Mentors:** Nan Li and Brandon Gallas

**Overview:**
The custom/HTT branch of caMicroscope is special instance of caMicroscope that is being used in an FDA project to collect validation data. After a pathologist logs on, he or she selects a batch and then an image within a batch to begin their evaluations. The evaluation task is collected with specific controls: buttons, scroll bars, numeric input. We would like to control the order the pathologists evaluate the batches and individual images with a “work list”. This work list will specify the task for each element to be completed. The tasks will be defined in modular pieces of code, allowing external investigators to modify old tasks and add new tasks, such as a comparative task that requires pathologists to view two images side-by-side.

**Current Status:** New

**Required Skills:** JavaScript

**Code Challenge:** Extract the current task from code base and write as a unique module called by the code base

**Source Code:** https://github.com/camicroscope/caMicroscope/tree/custom/HTT

***

**[8] Integrate an optical microscope with a camera and motorized stage - Collaboration with FDA**

**Mentors:** Nan Li and Brandon Gallas

**Overview:**
The FDA has created eeDAP, an evaluation environment for digital and analog pathology. eeDAP is a software and hardware platform for designing and executing digital and analog pathology studies where evaluation regions of interest (ROIs) in the digital image are registered to the real-time view on the microscope. This registration allows for the reduction or elimination of a large source of variability in comparing these modalities in the hands of the pathologist: the field of view (the tissue) being evaluated. There are many other research and commercial use cases for eeDAP. eeDAP is written in Matlab, which is commercial software that requires a license and is not designed for digital pathology image viewing and annotation. We would like to move the eeDAP features into caMicroscope. The user will be able to control a digital camera and an x-y programmable microscope stage, with caMicroscope.
It may or may not be useful to consider use of custom tile sources in openseadragon.

**Current Status:** New

**Required Skills:** JavaScript, Hardware Communication and Control

**Code Challenge:** Create a webservice which emulates a motorized camera: taking in the x position, y position, zoom, logging which motor actions would be needed to move the slide to this new position, and return some image. 

**Source Code:** https://github.com/camicroscope/caMicroscope

***
# Applying for GSOC

Mentors and evaluators usually look for:
* The proposal itself is clear relevant, and realistic.
* The student has demonstrated that they have the relevant skills to complete the proposal.
* The student has shown an interest in open source, especially caMicroscope. This includes community involvement.
* Code Challenges and other relevant demonstrations go above and beyond in some interesting way.

## Application Template

The following Template is provided to help organize all required information for a successful GSOC application. While following this template is not required, please be sure that your application is complete.

**1) Project Title:**

**2) Abstract / Project Summary**:

Summarize the project in your own words.

**3) Student Name:**

**4) Student Email and Slack username:**

**5) Potential Mentor(s):**

**6) Personal Background (Brief CV)**

**7) Project Goals**

(Enter as bullets)

..
     
..
     
..

**8) Project Schedule**

Break the timeline into periods of approximately 7 days

**9) Planned GSoC work hours**

Please indicate the work hours (including the timezone), that you hope to work on your project. 

**10) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Indicate any examinations or other personal commitments. 

**11) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).
