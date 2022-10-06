# how to update the humon lab docs

## Background
<p>&nbsp;</p> 

We're updating the docs that live on this repository- 
https://github.com/HuMoN-Research-Lab/HuMoN-Research-Lab.github.io
and are hosted via Github Pages at this URL - https://humon-research-lab.github.io/

The page is built via the `material` theme of mkdocs

mkdocs lives here - 
https://www.mkdocs.org/

Specifically the theme we are using lives here -
https://squidfunk.github.io/mkdocs-material/

This workflow is very similar to the one we will use to update the freemocap docs, except that the HuMoN Lab docs will be hosted via Github Pages while the freemocap docs are hosted via `readthedocs.io`
<p>&nbsp;</p> 

## How to guide - Update the humon research lab docs  
<p>&nbsp;</p> 

### Method 1: Using the Terminal
 Clone the repository on your computer using a terminal (I'm going to use a Windows Terminal, but it would look the same from any Command Prompt or powershell or whatever)
    - this assumes you gave `git` installed. If you don't google "how to install git"
- in the terminal
    -  `cd` to the location you want to store the docs
    -  type `git clone https://github.com/HuMoN-Research-Lab/HuMoN-Research-Lab.github.io
- open that folder in PyCharm
    - make sure to open the ENTIRE FOLDER, not  a file inside of it
- make a branch off the `main` branch
    - call it [your_name]/[some_description_of_what_youre_doing]
        - no spaces
        - keep it short, it doesn't matter
- Make a change to a document in the `/docs/` folder OR the configuration file `mkdocs.yml`
- You can PREVIEW your changes by entering the command `mkdocs serve` in the terminal
    - after you've installed `mkdocs-material` via `pip install -r requirements.txt`
- add new pages by adding them to `nav` in the `mkdocs.yml` file
    - detailed instructions here - https://www.mkdocs.org/getting-started/#adding-pages
- When you are happy with your changes:
  - commit your branch to Github
  - make a Pull Request (PR) onto the `main` branch
- When that PR is approved, it will automatically update the live docs site

### Method 2: GitHub Desktop
- Have Jon give you access to the freemocap foundation. This will allow you to make branches to the Humon Research Lab github repo. 

- Install Github Desktop and add make this repo be the 'Current Repository': https://github.com/HuMoN-Research-Lab/HuMoN-Research-Lab.github.io

- Create a new branch with your name and 'dev' in the title. Push the new branch. 

- Now you can start making changes to the repo...using Vscode, PyCharm, Obsidian, etc. Make a change to a document in the `/docs/` folder OR the configuration file `mkdocs.yml`.
- You can PREVIEW your changes by entering the command `mkdocs serve` in the terminal
    - after you've installed `mkdocs-material` via `pip install -r requirements.txt`
- add new pages by adding them to `nav` in the `mkdocs.yml` file
    - detailed instructions here - https://www.mkdocs.org/getting-started/#adding-pages
- When you are happy with your changes:
  - commit your branch to Github. Try to do this farely regularly so you don't commit a whole bucket of changes all at once, but rather a few at a time. 
  - make a Pull Request (PR) onto the `main` branch
- When that PR is approved, it will automatically update the live docs site
---

## Workflow for contributing to Troubleshooting 
- When you run into any issue that you eventually solve and you think someone else in the lab would benefit from knowing how you solved it, you should add it to the Troubleshooting folder. Here's a rough workflow to follow so we can attempt to have a standard-ish way of doing things. When making this workflow, I used this reference: [New Relic Troubleshooting Docs Guide](https://docs.newrelic.com/docs/style-guide/writing-docs/article-templates/troubleshooting-docs-guide/) and []
    
    ### 1. Problem
    
    - Provide a clear, concise description of the problem the user is trying to solve. Who, what, when, where?  

    ### 2. Solution(s)

    - Provide an ordered list of steps to guide someone through the solution. Copy and paste useful parts of the error codes. (No screen shots. Ideally, we want to be able to search the error codes themselves).

    ### 3. Cause(s)

    - A highlevel paragraph of why the error happened. 

    ### 4. Related info
    
    - A more indepth reason why the error occured. Jon, this one's for you :) 