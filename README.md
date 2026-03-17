# Watdev model template

This is a template repository for a Watdev model repository.

You can use this template as a base for running the model in a Github Workflow.

## Quick start

- Fork this repository to your github account (rename to a sensible name)
- Clone the forked repository locally

```bash
git clone https://github.com/{github-username}/{repository-name}
cd {repository name}
```

- Use [Swat Editor](https://swat.tamu.edu/software/swat-editor/) or some other tool to generate the typical HRU based input files.
- Copy the contents of TxtInOut into the local repository location.
- Test the model run locally using SWAT

```bash
docker run --rm  -v $(pwd):/swat_data -w /swat_data crazyzlj/swat:alpint-2012.683 swat2012.683.gfort.rel
```

- Commit and push local content to the github repository

```bash
git add .
git commit -a -m "{Sensible commit message}" 
git push
```

## Multiple scenarios

In many cases you will have multiple scenarios in your repository, each repository calculates the effect of certain Management Practices or Climate Scenarios.

Create a branch for each scenario. The structure of each of the branches will be similar.
The outputs of the scenario runs will be available in branch output in /{branchname}/output.zip

- main (general documentation)
- baseline (the baseline scenario)
- schenario1
- scenario2

