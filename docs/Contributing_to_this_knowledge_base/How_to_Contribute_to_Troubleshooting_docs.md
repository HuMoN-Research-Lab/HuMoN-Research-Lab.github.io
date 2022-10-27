## Workflow for contributing to Troubleshooting  

- When you run into any issue that you eventually solve and you think someone else in the lab would benefit from knowing how you solved it, you should add it to the Troubleshooting folder. Here's a rough workflow to follow so we can attempt to have a standard-ish way of doing things. When making this workflow, I used this reference: [New Relic Troubleshooting Docs Guide](https://docs.newrelic.com/docs/style-guide/writing-docs/article-templates/troubleshooting-docs-guide/). 

<p>&nbsp;</p>

**First:**  

1. Check out the troubleshooting folder in this repository to see if there is already a .md file in there with the category of error you're experiencing (like 'Mkdocs Errors' or 'running a freemocap session errors' or 'Blender Errors'). If there is already a file with your error category, simply add to the current file and just add a line (---) and a new secondary header (##) with your specific error problem. 
    - Add your troubleshooting solution following the loose framework below.

2. If there isn't a file with your error category, just create a new .md file inside the 'Troubleshooting' folder. In that new file, give it a reasonable header (#) so we all can understand the error category. 
    -  Add your troubleshooting solution following the loose framework below.

<p>&nbsp;</p>

See this [mkdocs errors troubleshooting doc](../Troubleshooting/Mkdocs_Errors.md) as an example of how to structure your contribution. 

<p>&nbsp;</p>


    # General Error Category
    
    ## More Specific Description of Error

    ### 1. Problem
    
    - Provide a clear, concise description of the problem the user is trying to solve. Who, what, when, where?  

    ### 2. Solution(s)

    - Provide an ordered list of steps to guide someone through the solution. Copy and paste useful parts of the error codes. (No screen shots. Ideally, we want to be able to search the error codes themselves).

    ### 3. Cause(s)

    - A highlevel paragraph of why the error happened. 

    ### 4. Related info
    
    - A more indepth reason why the error occured. Jon, this one's for you :)  

    ---
    