# Late Night Bayes

## What is it?

This is the GitHub Repo associated with the Late Night Bayes blog. The blog is an idea dump for any projects that I think are interesting but not worth investing the time it would take to write a rigorous paper. You can find out more details at [Late Night Bayes](latenightbayes.com).

## To my future self: How the heck do you publish new chapters?

*Stop being an idiot and read this before trying whatever stupid trick you're thinking of.* The website is generated using a series of R markdown files along with the bookdown package. 

Make whatever analysis notebook you want. Don't forget to number it since I don't specify what order to put the chapters (defaults to the name order of the files). Images go in \\images\\, datafiles go in \\data\\, and temporary files go in \\temp\\. Take advantage of temp to save the output from cells that take a long time to run, then switch those cells to "```{r, eval=FALSE}". This will save you a bunch of time on publishing.

Once you're ready to publish, open "LateNightBayes.Rproj". It will open up RStudio. Look for the "Build" tab, which I keep in the same panel as my "Environment" and "Plot" tabs. In the "Build" tab, there's a button "Build Book". Click that and give it a few minutes. Once it finishes running, \\_book\\ will be generated. This is a gitbook with all the necessary .css, .html, libraries, and subfolders with attached files. That's the folder that's generating [Late Night Bayes](latenightbayes.com). On Netlify, the website is set to build from the \\_book\\ directory of the LateNightBayes repo on the main branch.

The _output.yaml file used to contain other outputs, like a pdf and epub book. I removed these since there's an issue with R 4.2, TinyTex, and generating static images from .gif files. Now the only thing generated is a gitbook in the form of \\_book\\.