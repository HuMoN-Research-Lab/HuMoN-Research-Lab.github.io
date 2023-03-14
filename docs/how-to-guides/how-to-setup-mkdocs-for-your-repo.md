# How to setup mkdocs for your repo

###### tags: diataxis, how-to, mkdocs, github, documentation

## Introduction

This guide explains how to set up mkdocs documentation for your existing repository. If you are instead looking to edit this pages documentation, see [this guide instead](https://humon-research-lab.github.io/how-to-guides/how-to-update-these-docs/).

## How to guide

- First create a new conda environment in your terminal by running `conda create --name docs python=3.9`. Once that environment has been created, activate it with the command `conda activate docs`.
- Once your environment is installed and activated, install mkdocs and the material theme by running `pip install mkdocs mkdocs-material`.
- Navigate to the repo you want to create documentation for in your terminal by using the 'cd' command.
- Run the command `mkdocs new .` which creates a file `mkdocs.yml` and a `docs/` folder with a markdown file `index.md` in it (the period refers to the directory you're currently in).
- Edit the file `mkdocs.yml` in your ide of choice, so that:
    1. the `site name` is changed to what you want your site to be called
    2. after site name, add an empty line, then on the next line add `theme:`, add another line, press tab to indent, and add `name: material`
- You can then add markdown content to `index.md` in the `docs` folder, which will be the landing page for your website, or add new markdown files to the folder. 
- Before publishing, you may view your site by running `mkdocs serve` in your terminal. This will show you a local url you can put into your browser to view your site.
- Once you are happy with your site, build it by running `mkdocs build` in the terminal.
- Finally, run the command `mkdocs gh-deploy`. This should publish your website to your repository's github pages and show you a (now public) url to your site!