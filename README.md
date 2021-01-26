# caMicroscope GSoC 2021
<img src="https://avatars0.githubusercontent.com/u/12075069?s=200&v=4" width="150" height="150" align="left" style="padding:10px;"/> caMicroscope is a digital pathology image viewer with support for human/machine generated annotations and markups. The source code of the caMicroscope project can be found at https://github.com/camicroscope/caMicroscope, released with BSD 3-Clause License. In addition to the caMicroscope project, caMicroscope as an organization also hosts several related tools and products at https://github.com/camicroscope/

For 2021, the scope of GSOC projects have changed. Since the projects will be shorter, the camicroscope community will be able to focus on smaller interesting projects. We look forward to sharing our thoughts going forward, and thank you for your patience.

# Communicating with the mentors
We intend to use Slack as the primary medium of communication. The slack room at camicroscope.slack.com is used to discuss project ideas. You may join the caMicroscope Slack channel through our shared link - http://bit.ly/camicroscope
 
# List of Ideas
The following ideas were created with feedback from contributors and collaborators. Submissions need not come from the below list, but should have reasonable relevance to the caMicroscope organization and its goals. Please feel free to discuss these or other project ideas on the email list or Slack group.  
** More ideas are upcoming **

***

**[1] Machine Learning Smartpens**

**Mentors:**  Ryan Birmingham

**Overview:** 

This project would involve adapting pathology annotation tools to prefer following edges in the base image when close. This would also involve expanding the user functions surrounding annotation, such as moving points in the drawing. Specific UI flow is up to the implementer; perhaps it's more useful to leave drawings alone, but have a button which snaps drawings to the nearest edge when pushed.

**Current Status:** The current annotation tools perform point simplification after a user finishes drawing without any consideration of the base image.

**Required Skills:** JavaScript, tensorFlow.js

**Code Challenge:** Create a page or tool which performs edge detection on a given image and, given a point, returns the distance from that point to the closest edge.

**Source Code:** https://github.com/caMicroscope/caMicroscope

***

**[2] Cross-Slide Coordinated Viewing**

**Mentors:**  Nan Li

**Overview:** 

Often, it's useful for users to compare different results on an image. To facilitate this, caMicrocope supports viewing the same image with different results, such as heatmaps, segmentations, and annotations, in a coordinated fashion. Since adjacent tissue slice images are usually quite similar, it can be useful to have a similar coordination between different images.
This project focuses on creating a tool to allow a user to do this. The two different tissue samples may be differently situated in their images, and may require a user to change scale, position, and rotation to sync up the two images.

**Current Status:** The current coordinated view tools are used for different results on the same image, with no support for multiple images at once.

**Required Skills:** JavaScript, OpenSeadragon

**Code Challenge:** Link user interaction across two OpenSeadragon instances if a checkbox is checked, otherwise, let them move independently.

**Source Code:** https://github.com/caMicroscope/caMicroscope 

***

# Application Template

The students are encouraged to follow this template. However, they are not expected to strictly follow this template. They are rather advised to clearly include all the requested information in their application.

**1) Project Title:**

**2) Abstract / Project Summary**:

Summarize the project in your own words.

**3) Student Name:**

**4) Student Email and Slack username:**

**5) Potential Mentor(s):**

**6) Personal Background (Brief CV)**

**7) Project Goals / Major Contributions**

(Enter as bullets)

..
     
..
     
..

**8) Project Schedule**

Break the timeline into periods of approximately 7 days

**8.1) Community Bonding Period**

**8.2) Development Phase**

**8.3) Project Completion, testing, and documentation**

**9) Planned GSoC work hours**

GSoC students are expected to contribute an average of 18 hours per week. Please indicate the work hours (including the timezone), that you hope to work on your project. 

**10) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Please indicate if you have any lectures/classes, examinations, or other personal commitments. 

**11) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).
