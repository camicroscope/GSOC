# caMicroscope GSoC 2022
<img src="https://avatars0.githubusercontent.com/u/12075069?s=200&v=4" width="150" height="150" align="left" style="padding:10px;"/> caMicroscope is a digital pathology image viewer with support for human/machine generated annotations and markups. The source code of the caMicroscope project can be found at https://github.com/camicroscope/caMicroscope, released with BSD 3-Clause License. In addition to the caMicroscope project, caMicroscope as an organization also hosts several related tools and products at https://github.com/camicroscope/

For 2022, GSOC projects may be either full-time or half-time. Most project ideas could work in either format, albeit with different levels of scope. Contributors should specifically propose either a full-time or half-time project timeline, and adjust the scope accordingly. We look forward to sharing our thoughts going forward, and thank you for your patience.

# Communicating with the mentors
We intend to use Slack as the primary medium of communication. The slack room at camicroscope.slack.com is used to discuss project ideas. You may join the caMicroscope Slack channel through our shared link - http://bit.ly/camicroscope

# Code Challenges
Code Challenges submissions should demonstrate creativity, understanding of the project, and ability to execute on a project proposal. Submit code challenges for early review and feedback here: [caMicroscope | GSOC 2021 | code challenge submission](https://forms.gle/k4ZcH75UYG4y2tRJ7) 
 
# List of Ideas
The following ideas were created with feedback from contributors and collaborators. Project ideas are not listed in any particular oder. Submissions need not come from the below list, but should have reasonable relevance to the caMicroscope organization and its goals. Please feel free to discuss these or other project ideas on the email list or Slack group.  
** More ideas are upcoming **

***

**[1] Use Web Components**

**Primary Mentor:**  Akhil Rana

**Overview:** caMicroscope is written in javascript without the use of any frameworks. This has the benefit of making the code directly usable by browsers without transpilation, but has the side effect of making code less regular. We propose using something such as [Web Components](https://www.w3.org/TR/components-intro/) to make the caMicroscope viewer code more regular. This project may not include a complete refactor of caMicroscope, so good proposals would take into account which components to target.


**Current Status:** New Project

**Required Skills:** JavaScript, HTML, WebComponents

**Code Challenge:** A simple webapp demonstrating WebComponents.

**Project Size:** Short (175 Hour) or Long (350 Hour) depending on proposal

**Source Code:** https://github.com/caMicroscope/caMicroscope 

***

**[2] Client Driven Slide Tiling**

**Primary Mentor:**  Ryan Birmingham

**Overview:** The Cancer Whole Slide images that caMicroscope users interact with come in a variety of formats, but most of these are organized very similarly to the tiff format. As a result, we believe that we can write an image viewer or tile server for at least one such format entirely in the browser. There are multiple ways which this sort of task may be completed, including transpiling an existing library (Openslide or Bioformats) to javascript, or writing something entirely new.



**Current Status:** Some underdeveloped proof of concepts exist

**Required Skills:** JavaScript, C, Java, and/or Python

**Code Challenge:** Create a website which displays the values of [standard tiff tags](https://www.loc.gov/preservation/digital/formats/content/tiff_tags.shtml) for a user-selected tiff image.

**Project Size:** Short (175 Hour) or Long (350 Hour) depending on proposal

**Source Code:** https://github.com/camicroscope/iipimage (and likely a new repository for this project)

***


**[3] Administrative Functions Portal**

**Primary Mentor:**  Nan Li

**Overview:** caMicroscope is usually configured in a hosted environment with some deployment-specific configuration. Currently, this is done through editing configuration files on the server which populate a database. It would be much more user friendly if all of these functions could be accomplished with a web UI alongside other viewer functions. This project would involve migrating as many administrative functions as possible to the web UI.

**Current Status:** Work in Progress

**Required Skills:** JavaScript, HTML

**Code Challenge:** Create a basic CRUD app, such as a shopping list.

**Project Size:** Short (175 Hour) or Long (350 Hour) depending on proposal

**Source Code:** https://github.com/camicroscope/caMicroscope

***

**[4] Desktop and/or Mobile caMicroscope**

**Primary Mentor:**  Nan Li

**Overview:** Since biomedical datasets and research motivation comes in different scales, it’s important that there exist tooling setups to fit these different needs. While in many situations, collaborative online research is helpful, we aim to provide visualization and analysis tools to individual users as well. This project aims to create either a desktop or mobile standalone version of caMicroscope, following "Nanoborb", the previous iteration of this concept.

**Current Status:** Existing Project: Refactor or Recreation

**Required Skills:** JavaScript, Likely Python and/or Java, HTML

**Code Challenge:** Create an electron-based (or other web ui framework for python or java) application with persistent data storage.

**Project Size:** Short (175 Hour) or Long (350 Hour) depending on proposal

**Source Code:** https://github.com/camicroscope/nanoborb

***

**[5] Pathology Game**

**Primary Mentor:**  Ryan Birmingham

**Overview:** caMicroscope has a viewer component and support for machine learning models. Thus, we have the components to build an alternate version of the viewer to host a pathologist vs machine learning model game. This would serve as a demo of caMicroscope, a way to validate machine learning models, and could be fun or an informal training exercise for pathologists.

**Current Status:** New App

**Required Skills:** JavaScript, TensorFlow

**Code Challenge:** Make a clone/mvp of a game similar to geoguessr.

**Project Size:** Long (350 Hour)

**Source Code:** https://github.com/camicroscope/camicroscope

***


**[6] Role-Based Access Control Deployment Option**

**Primary Mentor:**  Yash Kumar Verma

**Overview:** In previous years, components for role based access control for caMicroscope have been developed. This task would focus on creating deployment configuration for caMicroscope to use these tools in production. This will likely also include some touch-up, additional functions, and documentation for the RBAC components.

**Current Status:** Components Exist

**Required Skills:** JavaScript, Docker/Kubernetes

**Code Challenge:** Docker Compose or Kubernetes Deployment of a series of services.

**Project Size:** Long (350 Hour)

**Source Code:** https://github.com/camicroscope/distro, https://github.com/camicroscope/rbac-admin

***

***


**[7] Improving on the real-time collaboration system**

**Primary Mentor:**  Vedant Nandoskar

**Overview:** In last year's GSOC season, we had built a real-time collaboration system  for caMicroscope allowing for remote users to work simultaneously on slides. Most features are based on websockets. Currently, the system supports the following features:

- Real-time two-way data communication of activity on slides.
- Security mechanism to the communication channels.
- Role based management of the communication channels.
- Private and Public channels.
- In-app group messaging.
- Integrated Video/Voice calling.

As extensive as the system is, it still needs refinements in terms of:

1. Handling socket communication 
2. A soft commit feature
3. Multiple collaboration rooms on a slide

&nbsp;
1. **Handling socket communication**
This would consist in optimising the way socket data is handled, transmitted and received before being rendered on the UI. Shortening/compression could also be integrated to allow for lesser network load.

2. **Soft commit feature**
The soft commit feature would allow for users to work on a slide without saving changes to the database. Something of the sort of a non-persistent datastore. The data in this store would only be saved in the database once the user clicks a 'commit' button. This is important so that the commits from multiple rooms on the same slide do not conflict or overwrite each other.

2. **Multiple collaboration rooms on a slide**
This feature consists in extending the existing collaboration rooms to share the same slide alongwith having a soft commit feature as described above.

**Current Status:** Real time collaboration system is in place.

**Required Skills:** JavaScript, Websockets, data handling, compression.

**Code Challenge:** Create a simple text editor allowing multiple users to edit the file. This text editor need not have formatting options, a simple texfield would do too. Integrate a simple soft commit feature with multiple collaboration rooms with it. Try to keep it simple without using JS frameworks, simple HTML, CSS, and JS would do.

Libraries you could use: 
- [https://socket.io/](Socket.io/) - for websockets implementation in JS.
- [https://ckeditor.com/](CKeditor) - (optional) for a readymade text editor.
**Project Size:** Long (350 Hour)

**Source Code:** 
- [Camicroscope](https://github.com/camicroscope/caMicroscope/tree/realtime)
- [Caracal](https://github.com/camicroscope/Caracal/tree/realtime)
- [Distro](https://github.com/camicroscope/Distro/tree/realtime)
***

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
