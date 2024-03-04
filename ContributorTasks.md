Welcome to caMicroscope! These contribution tasks are designed to smoothly onboard contributors, showcase skills, and propel the caMicroscope project forward. Tasks are neatly categorized and can be submitted as pull requests or issues. We recommend starting with the Introductory "Getting Started" and "Open Source Communication" categories.

Tasks beyond the introductory stage are scoped to be achievable within a few days to a week for contributors less familiar with caMicroscope. Remember, quality over quantity! A well-executed contribution, coupled with thorough documentation, speaks volumes about your open-source engagement.

No need to be an expert! These tasks are perfect for developing new skills and gaining hands-on experience. Most importantly, enjoy the process. If challenges arise or you need assistance, don't hesitate to start a discussion thread or open an issue. Take your time, experiment, and, if needed, ask for help (we recommend spending about an hour trying to troubleshoot on your own first; issues which take longer than that are good to document/discuss anyway, and will hopefully stop people from becoming frustrated) Thank you for working with us, and happy contributing!

Introductory: Getting Started (Not Directly Pull Request Changes)



* Clone caMicroscope and its repositories, especially distro
* Install Docker and Docker compose
* Run some version of caMicroscope locally (recommended develop.yml)
* Add a Slide to your instance of caMicroscope
* Experiment with the Viewer Tools
* Experiment with additional Tools

Introductory: Open Source Communication (Not Directly Pull Request Changes)



* Find or start a relevant discussion for a discussion-like topic
* Submit or comment on a relevant issue or pull request
* Specifically, make an issue or pull request on something which was unclear, with a proposed fix if applicable

Open Source Support



* Reproduce a bug on an open issue and comment about how you’ve done so

UI/UX Design and Programming



* Add a dark mode option for the caMicroscope app pages
* Report on a small part of caMicroscope’s UI at a task level and some ways it may be improved from a design perspective, including a plan to evaluate these proposed changes
* Diagnose and fix the caMicroscope viewer toolbar inconsistently resizing toolbar icons with changing browsers and window sizes
* Identify an app or task which is difficult on a mobile device (or other screen size) and propose a low to medium fidelity design solution

Machine Learning and Computer Vision



* Try another way to implement the “smart pens” segmentation annotation tool.
* Report on a relevant model or computer vision algorithm which could be helpful for caMicroscope’s viewer/annotations
* Add a (documented) segmentation ML model to the tfjs_models repository
* Add a (documented) classification ML model to the tfjs_models repository

Accessibility



* identify one accessibility bug using Web Content Accessibility Guidelines (WCAG) 2.1 standard levels within caMicroscope

Code Performance



* Report on a page/app/function which takes a long time for code execution
* In addition to the report, you can also propose an improvement (simpler is better!)
* Implement caching mechanisms to improve the overall speed and responsiveness of caMicroscope.

Testing



* Write tests for some existing caMicroscope functions
* After writing tests, set up github actions’ test suite to run these tests automatically
