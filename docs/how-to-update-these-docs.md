# how to update the humon lab docs

## background
we're updating the docs that live on this repository- 
https://github.com/HuMoN-Research-Lab/HuMoN-Research-Lab.github.io
and are hosted via Github Pages at this URL - https://humon-research-lab.github.io/

The page is built via the `material` theme of mkdocs

mkdocs lives here - 
https://www.mkdocs.org/

Specifically the theme we are using lives here -
https://squidfunk.github.io/mkdocs-material/

This workflow is very similar to the one we will use to update the freemocap docs, except that the HuMoN Lab docs will be hosted via Github Pages while the freemocap docs are hosted via `readthedocs.io`

## How to guide - Update the humon research lab docs
- clone the repository on your computer using a terminal (I'm going to use a Windows Terminal, but it would look the same from any Command Prompt or powershell or whatever)
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
- 