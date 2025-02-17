# caMicroscope GSoC 2025

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
- Some suggested [contributor tasks are highlighted here](ContributorTasks.md).
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


## IIP Image Tile Server Modernization 

**Overview:** The tileserver service, IIP Image, is essential for caMicroscope's ability to function. Since it breaks large images of various formats into pieces and returns them, the intermediate format of the tiles impacts how the images end up being displayed to the end users.

Fortunately, due to containerization, this quite tepermental software has been stable. However, this also means we have accumulated tech debt, and the IIP upstream codebase is well ahead of our server. We hope to be able to use modern features, especially losslessly compressed PNG encoding. This would require fixing or redoing the upgrades, which are quite substantial.

ALTERNATIVELY: If you can get a python or other stable and performant alternate implementation of a IIIF or DZI (or other openseadragon compatible protocol) which works with the WSIs we use, this may be done in place. For exactly this reason, though, focus on clarity and maintainability, especially if you take this route.

Please make a selection of high level method prior to proposal, if possible.

**Project Requirements:** 
 * Tile server should be able to support lossless png and other encodings
 * Tile server should be able to read Openslide images
 * Bonus, Tile server should be able to also read BioFormats Images

**Current Status:** Existing Codebase, Work in progress patch

**Required Skills:** C++, Image Processing, Web Services

**Difficulty:** Difficult

**Project Length:** Long (~350 hours)

**Source Code:** https://github.com/camicroscope/iipimage

**Primary Mentor:** Tony Pan

## RDF Support for caMicroscope

**Overview:** This project focuses on enhancing caMicroscope's data representation by incorporating a semantic layer. The goal is to provide a sophisticated framework for handling slides, annotations about slides, and annotations nested within other annotations. Through the use of semantic representation, we aim to create a more structured and meaningful way to organize and understand the data. This project involves starting this process by adding RDF support for caMicroscope and modeling the existing relationships in a way which can later be expanded.

**Project Requirements:** 
 * Interpreting caMicroscope's data and metadata in a documented semantic representation format
 * RDF + SPARQL endpoints for this data

**Required Skills:** Semantic Web

**Difficulty:** Medium 

**Project Length:** Long (~350 hours)

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Ryan Birmingham

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

**Primary Mentor:** Nan Li

## Eaglescope for caMicroscope Use Cases 

**Overview:** Eaglescope is a dashboard/cohort visualization tool and related project to caMicroscope. Currently using Eaglescope and caMicroscope together is a quite manual process. More pressingly, the use cases we've seen implemented have generally been for collection and slide level exploration (i.e. finding slide(s) which meet your criteria). However, lots of expert data is collected on regions of interest (ROIs) which are spatial. 

This project would involve expanding caMicroscope's API presentation layer to be more easily compatible with caMicroscope, as well as adding more visualizations to support meaningful views for groups of spatial annotation data.

**Project Requirements:** 
 * Add flat APIs for caMicroscope's existing to better work with Eaglescope
 * Add Eaglescope as a way to select Images and Annotations in caMicroscope
 * Add geospatial filtering to Eaglescope
 * Add at least one new visualiation for GEOJson Objects to Eaglescope

**Current Status:** Existing Codebase, Some Earlier Demos may exist.

**Required Skills:** UX, GEOJson, Data Visualization, JavaScript

**Difficulty:** Medium

**Project Length:** Short (~90 hours)

**Source Code:** https://github.com/sharmalab/eaglescope

**Primary Mentor:** Nan Li


## DICOMWeb Pathology Tile Support

**Overview:** caMicroscope usually is configured such that the whole slide imaging files are colocated with all of the caMicroscope components. However, in some cases, these slides may be split across other servers; one such standard for this is DICOM Web. WADO-RS defines a method by which frames of a DICOM pathology image may be retrieved. This project involves adding full functionality to caMicroscope to support rendering such images. At minimum, this would be a hook into caMicroscope's tile render engine (openseadragon), but would ideally include the ability to interact with these images fully by adding their URLs to caMicroscope's slide database.

Viewing frames of images can be accomplised through the frontend via openseadragon's custom tile source API or a separate html5 canvas overlay, or in the backend by adding an IIPimage interface.

**Project Requirements:** 
 * Able to view variously sized DICOM Path images usuing DICOM Web
 * UX flows to "register" such images in caMicroscope's Database

**Current Status:** Some Exploratory Work Done Previously

**Required Skills:** DICOMWEB, UX, JavaScript, Possibly C++

**Difficulty:** Medium

**Project Length:** Long (~350 hours)

**Source Code:** https://github.com/camicroscope/camicroscope

**Primary Mentor:** Ryan Birmingham


## Integrating Deep Learning Models to Classify Whole Slide Images

**Overview:** This project will develop software tools to combine multiple pre-trained deep learning models to develop models for classifying whole slide tissue images or image regions. The tools will be designed to provide a library and micro-service interfaces that can be utilized by other caMicroscope components, such as the caMicroscope Web user interfaces. 

The project is motivated by the rapidly increasing number of pre-trained or foundation models that are available in model repositories such as Hugging Face. Foundation models can reduce the cost of training task specific models. The goal of this project is to develop tooling to enable a user to combine multiple pre-trained models through feature fusion techniques or latent conditional diffusion methods and train classification models. The tool will allow the user to save the trained model and use it to analyze whole slide images or user-selected regions.  

Viewing frames of images can be accomplised through the frontend via openseadragon's custom tile source API or a separate html5 canvas overlay, or in the backend by adding an IIPimage interface.

**Project Requirements:** 
 * The toolkit should be able to integrate models from Hugging Face.
 * The toolkit should work with image patches (in jpeg or png formats) and whole slide tissue images
 * The toolkit should be accessible as a python library and via a micro-service REST interface 

**Current Status:** Existing code to use one pre-trained model to develop a classifier 

**Required Skills:** PyTorch, Python, Image Processing, REST APIs

**Difficulty:** Difficult

**Project Length:** Long (~350 hours)

**Source Code:** https://github.com/tkurc/wsi_classification_gsoc2024

**Primary Mentor:** Tahsin Kurc 


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
