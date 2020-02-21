# caMicroscope GSoC 2020
<img src="https://avatars0.githubusercontent.com/u/12075069?s=200&v=4" width="150" height="150" align="left" style="padding:10px;"/> caMicroscope is a digital pathology image viewer with support for human/machine generated annotations and markups. The source code of the caMicroscope project can be found at https://github.com/camicroscope/caMicroscope, released with BSD 3-Clause License. In addition to the caMicroscope project, caMicroscope as an organization also hosts several related tools and products at https://github.com/camicroscope/

This is the first year that caMicroscope plans to participate in GSoC as a mentoring organization. However, we have been an open source organization for 7 years since inception. Our GSoC mentoring team is composed of past GSoC organization administrators, mentors, and students from the other organizations that participated in the GSoC in the previous years.


# Communicating with the mentors
We intend to use Slack and mailing lists as the primary medium of communication. You may send an email to our mailing list camicroscope@googlegroups.com or use Slack camicroscope.slack.com to discuss project ideas. You may join the caMicroscope Slack channel through our shared link - http://bit.ly/camicroscope
 
# List of Ideas
The following ideas were created with feedback from contributors and collaborators. Submissions need not come from the below list, but should have reasonable relevance to the caMicroscope organization and its goals. Please feel free to discuss these or other project ideas on the email list or Slack group.  

***

**[1] Cancer Region of Interest Extraction and Machine Learning**

**Mentors:**  Ryan Birmingham and Insiyah Hajoori

**Overview:**

This project would involve extending the existing machine learning intergrations beyond marking up images, and allow users to fetch regions of interest from a given slide automatically. This would allow for users and scientists to train other models for tasks such as synthetic data generation. Specifically, this task would involve letting a user run a model on an image and download sections of the image based on model output.

The aim is to support a wider range of models and flexible use of their outputs. One such example is a two stage CNN described [here](https://arxiv.org/pdf/1803.04054.pdf). Currently, caMicroscope supports single stage networks showing results directly, but no provision to use those results in any other model. 

**Current Status:** Currently, caMicroscope supports uses of multiple types of models for markup, implemented with TensorFlow.js. Likewise, download of areas in an image given a bounding box is also supported.

**Required Skills:** JavaScript, TensorFlow.js (recommended)

**Code Challenge:** Using a machine learning toolkit of your choice, create a tool which identifies objects in the image, then returns positions in pixels corresponding to bounding boxes of a user-selected class of object in the image. For example, given an image with both cats and dogs, return bounding boxes for only cats.

**Source Code:** https://github.com/caMicroscope/caMicroscope 

**Slack Room:** interest-extraction 

***

**[2] Pathology Algorithm Development Workbench**

**Mentors:**  Nan Li and Erich Bremer 

**Overview:** 

This project would involve creating an application UI to serve as a workbench for development of pathology and image processing algorithms of different types. Desired functionality would focus on helping compare and tune models based upon their results in an interactive setting.

**Current Status:** Much of the baseline functionality exists, as do many algorithms, but there isn't a unified page or workflow for them.

**Required Skills:** JavaScript, HTML, CSS

**Code Challenge:** Create a simple webpage which incorporates user feedback to draw shapes, iteratively (that is, keep working on the same drawing using user feedback after each iteration).

**Source Code:** https://github.com/caMicroscope/caMicroscope 

**Slack Room:** dev-workbench 

***

**[3] High-Dimensional Medical Imaging**

**Mentors:**  Ryan Birmingham and Erich Bremer

**Overview:** 

This project would involve creating a server and basic client which can interact with high-dimensional data as if it were an image. Currently, slide images are transmitted as a series of RGB images corresponding to the area around where a user is viewing an image. The result of this project would work similarly, but for an arbitrary number of features.

**Current Status:** Current image serving is traditional RGB only.

**Required Skills:** JavaScript
**Optional Skills:** Python/Node.js/Java/etc (developer choice)

**Code Challenge:** Create a server which returns red, green, and blue channels of an image separately, and a client which recombines them into the original image.

**Source Code:** https://github.com/caMicroscope/caMicroscope

**Slack Room:** hd-imaging 

***

**[4] Machine Learning Smartpens**

**Mentors:**  Ryan Birmingham

**Overview:** 

This project would involve adapting pathology annotation tools to prefer following edges in the base image when close. This would also involve expanding the user functions surrounding annotation, such as moving points in the drawing. Specific UI flow is up to the implementer; perhaps it's more useful to leave drawings alone, but have a button which snaps drawings to the nearest edge when pushed.

**Current Status:** The current annotation tools perform point simplification after a user finishes drawing without any consideration of the base image.

**Required Skills:** JavaScript, tensorFlow.js

**Code Challenge:** Create a page or tool which performs edge detection on a given image and, given a point, returns the distance from that point to the closest edge.

**Source Code:** https://github.com/caMicroscope/caMicroscope

**Slack Room:** smartpens

***

**[5] Cross-Slide Coordinated Viewing**

**Mentors:**  Ryan Birmingham and Insiyah Hajoori

**Overview:** 

Often, it's useful for users to compare different results on an image. To facilitate this, caMicrocope supports viewing the same image with different results, such as heatmaps, segmentations, and annotations, in a coordinated fashion. Since adjacent tissue slice images are usually quite similar, it can be useful to have a similar coordination between different images.
This project focuses on creating a tool to allow a user to do this. The two different tissue samples may be differently situated in their images, and may require a user to change scale, position, and rotation to sync up the two images.

**Current Status:** The current coordinated view tools are used for different results on the same image, with no support for multiple images at once.

**Required Skills:** JavaScript, OpenSeadragon

**Code Challenge:** Link user interaction across two OpenSeadragon instances if a checkbox is checked, otherwise, let them move independently.

**Source Code:** https://github.com/caMicroscope/caMicroscope 

**Slack Room:** coordinated-view

***

**[6] Real-time DICOM Metadata Extractor**

**Mentors:**  Pradeeban Kathiravelu

**Overview:** 

[DICOM](https://www.dicomstandard.org/) is a common standard used to store and transfer medical images. In this project, the student will design and develop a real-time metadata extractor for DICOM images. The student may start from a metadata extractor from the set of DICOM images, and store the extracted metadata in a database (such as MongoDB). The metadata extractor should extract a set of attributes given by the user. In the latter phase, the student will extend the project to extract metadata from the images received real-time, by tracking the already extracted images. The tracking allows student to process metadata of only the new images, avoiding repeated processing. Additionally, the student may build APIs to support workflow executions on recently received DICOM data.

**Current Status:** We have built a Python-based prototype. However, we expect this project to be built in Java, and from the scratch, to avoid limiting the creativity of the student.

**Required Skills:** Java

**Code Challenge:** Create a simple Java program that can read DICOM metadata. Feel free to use existing libraries and modules. However, please cite the original sources if you borrow code online.

**Source Code:** New project. 

**Slack Room:** dicom-extract

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

Break the timeline into periods of 3 – 4 days

**8.1) Community Bonding Period**

**8.2) Development Phase**

**8.3) Project Completion, testing, and documentation**

**9) Planned GSoC work hours**

GSoC is expected to be a full time job, with 35 hours or more a week of contribution. Please indicate the work hours (including the timezone), that you hope to work on your project. 

**10) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Please indicate if you have any lectures/classes, examinations, or other personal commitments. 

**11) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).
