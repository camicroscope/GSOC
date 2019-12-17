# caMicroscope GSoC 2020
<img src="https://avatars0.githubusercontent.com/u/12075069?s=200&v=4" width="150" height="150" align="left" style="padding:10px;"/> caMicroscope is a digital pathology image viewer with support for human/machine generated annotations and markups. The source code of the caMicroscope project can be found at https://github.com/camicroscope/caMicroscope. In addition to caMicroscope project, caMicroscope as an organization also hosts several related tools and products at https://github.com/camicroscope/


# Communicating with the mentors
We intend to use Slack and mailing lists as the primary medium of communication. You may send an email to our mailing list camicroscope@googlegroups.com or use Slack camicroscope.slack.com to discuss the project ideas. You may join the caMicroscope slack channel through our shared link - http://bit.ly/camicroscope
 
# List of Ideas
The following ideas were created with feedback from contributors and collaborators. Submissions need not come from the below list, but should have reasonable relevance to the caMicroscope organization and its goals. Please feel free to discuss these or other project ideas on the email list or slack group.  

***

**[1] Machine Learning and Region of Interest Extraction**

**Mentors:**  Ryan Birmingham (rbirmin -at- emory.edu)

**Overview:**

This project would involve extending the existing machine learning intergrations beyond marking up images, and allow users to fetch regions of interest from a given slide automatically. This would allow for users and scientists to train other models for tasks such as synthetic data generation. 

**Current Status:** Currently, caMicroscope supports uses of multiple types of models for markup, implemented with TensorFlow-JS.

**Required Skills:** Javascript, TensorFlow-JS (recommended)

**Code Challenge:** Using a machine learning toolkit of your choice, create a tool which returns positions in pixels of areas depicting something (e.g. faces).

**Community and Code License:** https://github.com/caMicroscope/caMicroscope BSD 3-Clause License

***

**[2] Pathology Algorithm Development Workbench**

**Mentors:**  Nan Li (nan.li -at- emory.edu)

**Overview:** 

This project would involve creating an application UI to serve as a workbench for development of pathology and image processing algorithms of different types.

**Current Status:** Much of the basline functionality exists, as do many algorithms, but there isn't a unified page or workflow for them.

**Required Skills:** Javascript, HTML, CSS

**Code Challenge:** Create a simple webpage which incorperates user feedback to draw shapes, iteratively (that is, keep working on the same drawing using user feedback after each iteration).

**Community and Code License:** https://github.com/caMicroscope/caMicroscope BSD 3-Clause License

***

**[3] High-Dimensional Medical Imaging**

**Mentors:**  Ryan Birmingham (rbirmin -at- emory.edu)

**Overview:** 

This project would involve creating a server and basic client which can interact with high-dimensional data as if it were an image.

**Current Status:** Current image serving is traditional RGB only.

**Required Skills:** python/nodeJs/Java/etc (developer choice), Javascript

**Code Challenge:** Create a server which returns red, green, and blue channels of an image separately, and a client which recombines them into the original image.

**Community and Code License:** https://github.com/caMicroscope/caMicroscope BSD 3-Clause License

***

**[4] Machine Learning Smart Pens**

**Mentors:**  Ryan Birmingham (rbirmin -at- emory.edu)

**Overview:** 

This project would involve adapting pathology annotation tools to prefer following edges in the base image when close. This would also involve expanding the user functions surrounding annotation, such as moving points in the drawing. 

**Current Status:** The current annotation tools perform point simplification after a user finishes drawing.

**Required Skills:** Javascript, tensorFlow.js

**Code Challenge:** Create a page or tool which performs edge detection on a given image and, given coordinates, returns the distance to the closest edge.

**Community and Code License:** https://github.com/caMicroscope/caMicroscope BSD 3-Clause License

***

**[5] Cross-Slide Coordinated Viewing**

**Mentors:**  Ryan Birmingham (rbirmin -at- emory.edu)

**Overview:** 

This project would involve letting a user view two slides in such a way that when a user pans or zooms the effect is the same on both images. This is intended for showing different stains on similar tissue.

**Current Status:** The current coordinated views only focus upon the same image with different results or annotations.

**Required Skills:** Javascript, openSeaDragon

**Code Challenge:** Link user interaction across two openseadragon instances if a checkbox is checked, otherwise, let them move independently.

**Community and Code License:** https://github.com/caMicroscope/caMicroscope BSD 3-Clause License

***

**[6] Real-time DICOM Metadata Extractor**

**Mentors:**  Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu)

**Overview:** 

[DICOM](https://www.dicomstandard.org/) is a common standard for to store and transfer medical images. In this project, the student will design and develop a real-time metadata extractor for DICOM images. The student may start from a metadata extractor from the set of DICOM images, and store the extracted metadata in a database (such as MongoDB). The metadata extractor should extract a set of attributes given by the user. In the latter phase, the student will extend the project to extract metadata from the images received real-time, by tracking the already extracted images. The tracking allows student to process metadata of only the new images, avoiding repeated processing. Additionally, the student may build APIs to support workflow executions on recently received DICOM data.

**Current Status:** We have built a Python-based prototype. However, we expect this project to be built in Java, and from the scratch, to avoid limiting the creativity of the student.

**Required Skills:** Java

**Code Challenge:** Create a simple Java program that can read DICOM metadata. Feel free to use existing libraries and modules. However, please cite the original sources if you borrow code online.

**Community and Code License:** New project. Tentatively, BSD 3-Clause License

***

