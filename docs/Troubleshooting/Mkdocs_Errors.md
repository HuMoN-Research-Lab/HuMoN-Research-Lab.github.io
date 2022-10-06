# Mkdocs_Errors  


## Problem: 
When trying to preview changes made to freemocap documentation repo using the command `mkdocs serve` in the terminal, I got the following error:



    (base) kileyhartigan@Kileys-MacBook-Pro documentation % mkdocs serve
    INFO     -  Building documentation...
    ERROR    -  Config value: 'theme'. Error: Unrecognised theme name: 'material'. The available installed themes are: mkdocs, readthedocs
    ERROR    -  Config value: 'markdown_extensions'. Error: Failed to load extension 'pymdownx.snippets'.
            ModuleNotFoundError: No module named 'pymdownx'
    Aborted with 2 Configuration Errors!
<p>&nbsp;</p>

## Solution(s)
Skipping to the end of many things I tried:  
1. Make sure you're operating in a virtual environment. 
2. Once you're in your v-env, Update mkdocs and then install the server theme. To do these, enter these commands into the terminal: 
`pip install -U mkdocs`  (This command updates mkdocs)   
`pip install mkdocs-material` (This command installs the theme for the mkdocs server)
3. Now typing the command  
`mkdocs serve`  
into the terminal should give you a url that renders a static local site for you to check your changes. 
<p>&nbsp;</p>

## Cause(s)
1. The first problem was that I had an out of date version of mkdocs, so it didn't recognize the version of markdown my system was using.  
2. The second problem was that I hadn't installed the right theme.
<p>&nbsp;</p>

## Related info
The original error had a line that said: `...failed to load extension 'pymdownx.snippets'.`
  Stackoverflow and google helped me with a suggestion to force install pymdown like this...

    (base) kileyhartigan@Kileys-MacBook-Pro documentation % pip install pymdown-extensions --force
    Collecting pymdown-extensions
    Downloading pymdown_extensions-9.5-py3-none-any.whl (217 kB)
        |████████████████████████████████| 217 kB 517 kB/s 
    Collecting markdown>=3.2
    Downloading Markdown-3.4.1-py3-none-any.whl (93 kB)
        |████████████████████████████████| 93 kB 3.1 MB/s 
    Collecting importlib-metadata>=4.4
    Using cached importlib_metadata-4.12.0-py3-none-any.whl (21 kB)
    Collecting zipp>=0.5
    Downloading zipp-3.8.1-py3-none-any.whl (5.6 kB)
    Installing collected packages: zipp, importlib-metadata, markdown, pymdown-extensions
    Attempting uninstall: zipp
        Found existing installation: zipp 3.4.1
        Uninstalling zipp-3.4.1:
        Successfully uninstalled zipp-3.4.1
    Attempting uninstall: importlib-metadata
        Found existing installation: importlib-metadata 4.12.0
        Uninstalling importlib-metadata-4.12.0:
        Successfully uninstalled importlib-metadata-4.12.0
    Attempting uninstall: markdown
        Found existing installation: Markdown 3.3.7
        Uninstalling Markdown-3.3.7:
        Successfully uninstalled Markdown-3.3.7
    ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
    mkdocs 1.3.1 requires Markdown<3.4,>=3.2.1, but you have markdown 3.4.1 which is incompatible.
    Successfully installed importlib-metadata-4.12.0 markdown-3.4.1 pymdown-extensions-9.5 zipp-3.8.1

This helped me start looking at what version of markdown I was using and ultimately realized I could simply upgrade mkdocs to the newest version, which ultimately solved the markdown version issue.  

 

