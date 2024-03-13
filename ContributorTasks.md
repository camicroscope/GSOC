Welcome to caMicroscope! These contribution tasks are designed to smoothly onboard contributors, showcase skills, and propel the caMicroscope project forward. Tasks are neatly categorized and can be submitted as pull requests or issues. We recommend starting with the Introductory "Getting Started" and "Open Source Communication" categories.

Tasks beyond the introductory stage are scoped to be achievable within a few days to a week for contributors less familiar with caMicroscope. Remember, quality over quantity! A well-executed contribution, coupled with thorough documentation, speaks volumes about your open-source engagement.

No need to be an expert! These tasks are perfect for developing new skills and gaining hands-on experience. Most importantly, enjoy the process. If challenges arise or you need assistance, don't hesitate to start a discussion thread or open an issue. Take your time, experiment, and, if needed, ask for help (we recommend spending about an hour trying to troubleshoot on your own first; issues which take longer than that are good to document/discuss anyway, and will hopefully stop people from becoming frustrated) Thank you for working with us, and happy contributing!

## Introductory: Getting Started (Not Directly Pull Request Changes)



* [Clone caMicroscope and its repositories](#how-to-clone-a-repository), especially distro
* [Install Docker](#installing-docker) and Docker compose
* Run some version of caMicroscope locally (recommended develop.yml)
* Add a Slide to your instance of caMicroscope
* Experiment with the Viewer Tools
* Experiment with additional Tools

  ### How to clone a repository
  1. Go to the repository you want to clone and copy the URL.
  2. Open your command-line interface. To open this, search for “Command Prompt” on your Windows PC or “Terminal” if you’re using macOS/Linux.
  3. Use the `cd` command to navigate to the directory where you want to store the local copy of the repository.
  4. Use the `git clone` command followed by the URL of the repository to clone the repository. It should look like this:
      `git clone https://github.com/camicroscope/Distro`
  5. After entering the command, press Enter.
  Git will download all the files from the remote repository and create a local copy in your current directory. Once the process is complete, you should see a message indicating that the repository has been cloned successfully.

  Redo steps 1 - 5 for all the repositories you want to clone.

  ### Installing Docker
  **On a Windows PC:**
  1. Ensure that your Windows version meets the system requirements for Docker. Docker for Windows requires 64-bit Windows 10 Pro, Enterprise, or Education (Build 16299 or later) with Hyper-V enabled. You can check your Windows version by going to Settings > System > About.
  2. Go to the Docker website and download Docker Desktop for Windows. You can find the download link here: https://www.docker.com/products/docker-desktop
  3. Once the download is complete, double-click the downloaded installer file (typically named Docker Desktop Installer.exe) to start the installation process.
  4. Follow the installation wizard prompts to complete the installation. You may need to grant permissions or make configuration choices during the process.
  5. Once the installation is complete, Docker Desktop should be installed and running on your Windows PC. You should see the Docker icon in the system tray.
  To verify that Docker is installed correctly, open a command prompt and run the following command:
  
  `docker --version`

  You should see the version number of Docker displayed in the output if the installation was successful

  **On macOS:**
  1. Visit the Docker website and download Docker Desktop for Mac from https://www.docker.com/products/docker-desktop.
  2. Once the download is complete, open the downloaded .dmg file by double-clicking it. Drag the Docker icon to the Applications folder to install Docker Desktop.
  3. After installation, open Launchpad or use Spotlight search to find and launch Docker Desktop.
  4. On macOS Catalina (10.15) and later, Docker Desktop requires permission to install a system extension. Follow the on-screen prompts to allow the installation.

 

## Introductory: Open Source Communication (Not Directly Pull Request Changes)



* Find or start a relevant discussion for a discussion-like topic
* Submit or comment on a relevant issue or pull request
* Specifically, make an issue or pull request on something which was unclear, with a proposed fix if applicable

## Open Source Support



* Reproduce a bug on an open issue and comment about how you’ve done so

## UI/UX Design and Programming



* Add a dark mode option for the caMicroscope app pages
* Report on a small part of caMicroscope’s UI at a task level and some ways it may be improved from a design perspective, including a plan to evaluate these proposed changes
* Diagnose and fix the caMicroscope viewer toolbar inconsistently resizing toolbar icons with changing browsers and window sizes
* Identify an app or task which is difficult on a mobile device (or other screen size) and propose a low to medium fidelity design solution

## Machine Learning and Computer Vision



* Try another way to implement the “smart pens” segmentation annotation tool.
* Report on a relevant model or computer vision algorithm which could be helpful for caMicroscope’s viewer/annotations
* Add a (documented) segmentation ML model to the tfjs_models repository
* Add a (documented) classification ML model to the tfjs_models repository

## Accessibility



* identify one accessibility bug using Web Content Accessibility Guidelines (WCAG) 2.1 standard levels within caMicroscope

## Code Performance



* Report on a page/app/function which takes a long time for code execution
* In addition to the report, you can also propose an improvement (simpler is better!)
* Implement caching mechanisms to improve the overall speed and responsiveness of caMicroscope.

## Testing



* Write tests for some existing caMicroscope functions
* After writing tests, set up github actions’ test suite to run these tests automatically
