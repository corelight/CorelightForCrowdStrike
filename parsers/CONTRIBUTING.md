# How to develop the parser 

Parser processes log data and should normalize your data to [CPS standard](https://library.humio.com/logscale-parsing-standard/pasta.html).
Follow instructions below to create and manage a parser effectively.

## Steps to develop a parser

1. **Setup your parser**
   - Use the parser template available in your repository under the [parsers](parsers/) folder.
   - In the Parser Management Interface of the Falcon NG-SIEM, import the template provided in this repository.
   - For assistance with importing the parser template please read the "Guide - Falcon NG SIEM: HEC Connector Setup Overview" document.

2. **Extract fields from logs**
   Use available parsing methods based on your log format:
   - JSON logs: [parseJson()](https://library.humio.com/data-analysis/functions-parsejson.html)
   - CSV logs: [parseCSV()](https://library.humio.com/data-analysis/functions-parsecsv.html)
   - LEEF or CEF logs: [parseLEEF()](https://library.humio.com/data-analysis/functions-parseleef.html), [parseCEF()](https://library.humio.com/data-analysis/functions-parsecef.html)
   - Syslog format: Use [regex](https://library.humio.com/data-analysis/functions-regex.html) for custom extraction.

3. **Add log samples**
   - Click "Add a Test" in the interface to attach the first log sample.
   - Add additional samples representing different event types from your data source.
   - Log samples should be anonymized.

4. **Finalize and export**
   - Once the parser is complete, export it from the Falcon console.
   - Add the exported parser to the repository under the parsers directory.

## Helpful Resources

To expedite development, refer to these guidelines and documentation:

- **Parser development guidelines:**
  - [Parser Guideline](https://library.humio.com/logscale-parsing-standard/pasta-parser-guidelines.html)
  - [Parser Best Practices](https://library.humio.com/integrations/packages-developer-guidelines-assets-parsers.html)
  - [Anonymising logs](https://library.humio.com/logscale-parsing-standard/pasta-parser-guidelines-sample.html)

- **Vendor and module rules:**
  - [Vendor guidelines](https://library.humio.com/logscale-parsing-standard/pasta-vendors.html)
  - [Module rules](https://library.humio.com/logscale-parsing-standard/pasta-event-module.html)

- **CPS vs ECS:** [CPS Parser Guidelines](https://library.humio.com/logscale-parsing-standard/pasta-ecs.html)

- **Parser Management UI**
  - Navigate to the URL https://<falcon-url>/data-connectors/parsers
  - [Parser Development Guide - Creating parsers](https://library.humio.com/data-analysis/parsers-create.html)

- **Parser Naming Convention**
  - Format: `<vendor>-<product>-<sub-product>` where subproduct is optional
  - Examples: `microsoft-365` or `microsoft-azure-nsg`

## Submitting your parser

Once your parser is complete, submit it via pull request. It will allow us to review, discuss and approve your changes before merging them into the main branch.

### Pull request workflow

Here's a step-by-step pull request process:

1. **Create a branch**
   - Create a new branch off of the main.
   - Name it e.g. `feature/new-parser`

2. **Make changes**
   - Add parser, update the readme.md and include changelog

3. **Commit changes**
   - Write a clear and informative commit message for each change.

4. **Push changes**
   - Push your branch to the remote repository.

5. **Open a pull request**
   - In the web interface, open a pull request targeting the main or base branch

6. **Review process**
   - We will review your changes, provide feedback, and request updates if necessary.

7. **Update the pull request**
   - If necessary, make more changes, which automatically update the pull request.

8. **Approval**
   - Once approved, the changes can be merged into the main branch.

9. **Merge the pull request**
   - Merge the pull request into the main branch, delete the branch if no longer needed.

We start the process to publish your parser in Falcon NG-SIEM platform
