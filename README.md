# caMicroscope GSoC 2024

<h2 align="center">
  <a href="http://camicroscope.org/"><img src="https://avatars2.githubusercontent.com/u/12075069?s=400&v=4" style="background-color:rgba(0,0,0,0);" height=230 alt="camicroscope: a web-based image viewer optimized for large bio-medical image data viewing"></a>
</h2>

caMicroscope serves as a digital pathology image viewer, supporting human and machine-generated annotations and markups. The project's source code is available on GitHub at [caMicroscope GitHub Repository](https://github.com/camicroscope/caMicroscope) under the BSD 3-Clause License.

**caMicroscope Organization:**

- The caMicroscope organization hosts various related tools and products, accessible at [caMicroscope GitHub Organization](https://github.com/camicroscope/).

**Communication Channels:**

- **General Communication:** GitHub discussion forums are the primary communication channels.
- **GSOC-specific Communication:** Utilize the [GSOC Forum](https://github.com/camicroscope/GSOC/discussions) for GSOC-related discussions, including project ideas, timelines, and advice.
- **Organization-wide Questions:** For caMicroscope organization-wide questions not directly related to GSOC, use the [general forum](https://github.com/orgs/camicroscope/discussions).
- **Specific Communication:** Issues or discussions on individual repositories should be used for relevant and specific communication.
- **Private Communication:** For private communication with mentors, please email gsoc@camicro.org.

**Selection and "Code Challenges":**

- The caMicroscope mentor/admin team is reevaluating student selection processes. Emphasizing meaningful contributions to caMicroscope over disconnected demos is the priority.
- Refer to the [contribution guide](https://camicroscope.org/contributing.html) for details on making meaningful contributions.

**List of Ideas:**

- Project ideas have been compiled with input from contributors and collaborators.
- Ideas are not listed in any specific order.
- Submissions are not limited to the provided list but should be relevant to caMicroscope organization goals, see the [roadmap document](https://camicroscope.org/roadmap.html) for more guidance.
- Discussion on project ideas is encouraged through the [GSOC Forum](https://github.com/camicroscope/GSOC/discussions).
- Each idea has a list of project requirements which represent the minimum which must be completed to pass.

***

## High Dimensional Imaging Support

**Overview:** Most of the whole slide image data that we see are RGB images, representing the direct reading from an optical scanner on a tissue sample. This, combined with chemical stains on the image, provides a way to let experts assess an image based on inferences of relative color (e.g. H&E slide pink-purple ratio).
Sometimes, the spatial data represented is not the direct RGB values from a scanner. In this case, we encode three values as RGB. However, caMicroscope does not support datasets which have a spatial representation for more than three channels.
This project aims to add the backend support and frontend interactions to let users make sense of higher-dimensional data via multi-channel imaging support. This should likely be accomplished by adding a supplementary tile server which can read one channel at a time and return it as pyramidal images dynamically, and a user interface to let users select and mix such channels.

**Project Requirements:** 
 * Microservice to read multi-channel images with channel selection and return tiles in IIIF or DZI (or another Openseadragon compatible format)
 * Documented API for this microservice
 * Integrated with the caMicroscope UX, codebase, and deployment

**Required Skills:** Image Processing, User Experience

**Difficulty:** Medium 

**Project Length:** Long (~350 hours)

**Source Code:** New Project

**Primary Mentors:** Ryan Birmingham

## Exploratory Annotation Interaction

**Overview:** Annotating images is an essential feature of caMicroscope, and this can be accomplished in a variety of different ways. Ultimately, the goal is to let a user share their understanding and perspective, which can be centered on a region of interest of a slide, and an entire slide, or a set of slides at once. This project involves basic research and creating multiple varied prototypes of new annotation UX workflows in order to allow for collected data to reflect the perspective and expertise of users.

**Project Requirements:** 
 * At least three novel and distinct functional annotation prototypes
 * Documentation covering the use and design goals for each of these prototypes
 * Integrated with the caMicroscope UX and codebase
   
**Required Skills:** User Experience, Data Visualization

**Difficulty:** Medium 

**Project Length:** Long (~350 hours)

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Nan Li



## Accessibility Testing and Improvement

**Overview:** This project aims to improve the accessibility of caMicroscope's user interactions (focus on Slides and annotation module and administration. There are some limitations for the accessibility of the slide viewer) and add automatic testing as possible to ensure that further changes continue to uphold accessible usability. This would include integration of automatic testing tools (such as Axe, Pa11y, or Google Lighthouse) and compliance with the Web Content Accessibility Guidelines (WCAG) international standard.

**Project Requirements:** 
 * Automatic reports for caMicroscope app pages and documentation pages according to some existing accessibility standard
 * Changes which lead to a meaningful improvement in these reports' results
 * Revision of user documentation with respect to accessibility and any changes made

**Required Skills:** User Experience, Accessibility (a11y), CI/CD Testing

**Difficulty:** Medium 

**Project Length:** Short (~90 hours)

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Ryan Birmingham

## Image Classification using Foundation Models
**Overview:** This project will explore the utility of pre-trained and foundation AI models to carry out patch-level classification tasks in whole slide tissue images. A pre-trained or foundation model can be used as an encoder to train a task specific model. In our project, the task specific model will classify image patches extracted from whole slide images. Using a pre-trained or foundation model can help reduce training costs, by reducing the volume of training data and/or training a simpler model. It can also result in more robust and more accurate models. This project will primarily use models available at huggingface (https://huggingface.co). It will implement software components that: (1) will allow a user to search for and download a pre-trained or foundation model from the huggingface repository, (2) select a classification network from a collection of classification network implementations, (3) train the selected classification network with the pre-trained/foundation model as the encoder, and (4) apply the trained model on patches in a whole slide image.  

**Project Requirements:** 
 * A documented method for training a classification model using a pre-trained or foundation model
 * Implementation of this method as a set of software components
 * Integration of the components with caMicroscope
   
**Current Status:** New backend and frontend components

**Required Skills:** UX, Artificial Intelligence, Pytorch, Micro-services

**Difficulty:** High

**Project Length:** Long (~350 hours)

**Source Code:** http://github.com/camicroscope/camicroscope 

**Primary Mentor:** Tahsin Kurc

## Semantic Data Export and Exploration

**Overview:** This project focuses on enhancing caMicroscope's data representation by incorporating a semantic layer. The goal is to provide a sophisticated framework for handling slides, annotations about slides, and annotations nested within other annotations. Through the use of semantic representation, we aim to create a more structured and meaningful way to organize and understand the data.

The project involves the development of interactive features, allowing users to seamlessly navigate through the semantic layers, expand or collapse nested annotations, and gain a comprehensive understanding of the relationships between slides and annotations. This holistic approach aims to improve the overall user experience by offering a clearer and more insightful view of the complex data interactions within caMicroscope.

**Project Requirements:** 
 * Interpreting caMicroscope's data and metadata in a documented semantic representation format
 * At least one novel visualization, app, or other way to understand the semantic relationships of caMicroscop data
 * Integrated with the caMicroscope UX and codebase

**Required Skills:** Semantic Web

**Difficulty:** Difficult 

**Project Length:** Medium (~175 hours)

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Ryan Birmingham

## Quality Triage via Image Visualization and Annotation

**Overview:** In caMicroscope, images are often acquired in batches, such as during the digitization of multiple samples. These batches, intended to share common features, occasionally face issues like errors in staining, scanning, or labeling. This project addresses these challenges by enabling users to efficiently triage multiple slides visually. Users can add slide-level annotations, such as quality scores or flags indicating a need for re-scanning. This approach ensures a rapid and comprehensive assessment of slides, enhancing the overall quality of datasets within caMicroscope. By providing a quick and intuitive means to identify and address issues, the project significantly contributes to the platform's goal of maintaining high-quality, accurate datasets for robust medical imaging analysis.

**Project Requirements:** 
 * A web application (within caMicroscope) which is able to let a user interactively view multiple slides at once and collect data from the user about those slides.
 * User documentation for this application extending caMicroscope's user documentation
 * Integrated with the caMicroscope UX and codebase

**Required Skills:** User Experience, Image Visualization

**Difficulty:** Easy 

**Project Length:** Short (~90 hours)

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Nan Li

## Pathologist Annotation Behavior Report

**Overview:** caMicroscope is a widely used open-source end-to-end platform for digital pathology. Many pathologists use caMicroscope to annotate WSI cases in their daily work. How pathologists annotate the slide and the different behaviors that different pathologist works on the same slide are interesting questions. It is a good idea to collect and track pathologists’ annotation behavior in caMicroscope. Currently, caMicroscope only tracks the center position and zoom level of the user view. We propose an implementation intended for improving how to track the pathologist annotation behaviors and generating a pathologist behavior report in various formats such as image and pdf. The behavior report generally has the Pathologist’s view on a slide in  a timeline and the pathologist's actions in the slide viewer.

**Project Requirements:** 
 * Extend and improve the "log" data from caMicroscope when it is collected
 * A web application (within caMicroscope) which is able to interpret and visualize user behavior data
 * User documentation for this application extending caMicroscope's user documentation
 * Integrated with the caMicroscope UX and codebase

**Required Skills:** Javascript, HTML CSS, MongoDB, Web Backend

**Difficulty:** Easy 

**Project Length:** Short (~90 hours)

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Nan Li

## Eaglescope Automatic Configuration

**Overview:** Eaglescope is a web application for exploratory analysis of high-dimensional datasets, especially biomedical datasets. This tool has been designed primarily to focus on cohort identification, that is to identify a set of criteria which produce distinct or interesting data. Right now, in order to create a dashboard, the entire layout needs to be specified in a configuration manifest. However, this has the side effect of requiring that users already understand the data well enough to select which possible visualizations would be most interesting.
This project, Eaglescope Automatic Configuration, aims to provide instant statistical insight into which fields or combinations of fields can be best represented in the various different visualizations implemented in Eaglescope. This would have the added bonus of letting a user quickly explore a new dataset without writing any configuration. This has been proposed as a short project, and would focus on classical statistical methods. 

**Project Requirements:** 
 * A documented method for deciding which visualizations work with a given tabular dataset
 * Implementation of this method in Eaglescope such that it is used when no configuration is provided
 * Integrated with the Eaglescope UX and codebase

**Current Status:** New frontend application

**Required Skills:** UX, JavaScript, AI Recommender Systems, TensorFlow or other Web-compatible ML Toolkit

**Difficulty:** Medium

**Project Length:** Medium (~175 hours)

**Source Code:** https://github.com/sharmalab/eaglescope

**Primary Mentor:** Ryan Birmingham

&nbsp;
***
# Applying for GSOC

Mentors and evaluators typically look for the following:

- The proposal is clear, relevant, and realistic.
- The contributor has demonstrated the relevant skills to complete the proposal.
- The contributor has shown an interest in open source, especially caMicroscope, including community involvement.

## Application Template

The following template is provided to help organize all required information for a successful GSOC application. While following this template is not required, ensure that your application is complete.

**1) Project Title:**

**2) Abstract / Project Summary:**

Summarize the project in your own words.

**3) Contributor Name:**

**4) Contributor Email and Slack username:**

**5) Potential Mentor(s):**

**6) Personal Background (Brief CV)**

**7) Project Goals**
Describe specific outcomes, measurable or otherwise, as bullets.

**8) Detailed Project Proposal**

Describe what you propose to do for the project.

**9) Project Schedule**

Break the timeline into periods of approximately 7 days. Be clear on project size and timeframe, in compliance with google's requirements.
We also highly recommend including a something to show organization-wide as a demo in advance of both midterm and final evaluations to both show off your hard work, and elicit feedback beyond your mentor(s).

**10) Planned GSoC work hours**

Please indicate the work hours (including the timezone) that you hope to work on your project.

**11) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Indicate any examinations or other personal commitments.

**12) Open Source and Skills**

Include and explain your open-source contributions, and explain them as needed. Additionally, highlight your relevant skill set to complete this project. Ideally, there would be some overlap between your open-source portfolio and the skillset, showing familiarity with relevant pieces of caMicroscope's codebase.
