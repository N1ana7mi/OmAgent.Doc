# 📖 Introduction

> OmAgent is a LLMs(Large Language Models) powered framework for solving complicated AI tasks. 

OmAgent supplys a more universal simplified module for tasks in different domains, streamlining the application of Agents across various fields.:
> 
> - `Omagent-core` : Base abstractions and OmAgent Expression Language.
> - `Engine` : `Engine` is an extension of  `Omagent-core` aimed at endowing OmAgent with different capacities in additional to general task, like **Complex Visual Reasoning Tasks**, **Video Understanding, Visual Generation & Editing.**  It will contain customized ****definitions based on the class of ****`Omagent-core` .
> - `Workflows` : Define the customized llm, node, loop, tool information for personalized task.

# Opensource libraries

- `omagent-core` as the base construction and 




# Quick Start


### GitHub Pages

#### Hosting Site

To host this template on GitHub Pages do the following:  

1. Log into GitHub if you have not done so already
2. Tap the **Use this template** button in the upper-right of this GitHub Repository and choose **Create a new repository**
3. Enter a name for your new Repository and then tap the **Create repository** button
4. Once your new Repostitory is created go to **Settings**, then select **Pages** from the left-hand sidebar, and under **Branch** choose **main** and then tap the **Save** button
5. Wait a minute or two and refresh the same **Pages** page - once your site is ready a message will be displayed at the top of the screen along with a site link and a **Visit site** button

#### Editing Content

How about editing the content of your new Docsify site on GitHub Pages? View the Markdown page you want to edit (for example, **README.md**) and tap the **Pencil Icon**, then save any changes by tapping the green **Commit changes...** button. In just a few moments the Docsify site will be automatically updated to reflect those changes.

### Viewing Locally 
Run `npx serve .` (Node.js users) or `python -m http.server 8000` (Python users) in the repo folder to serve run locally.

## Docsify Documentation

To learn more about using Docsify, visit https://docsify.js.org.






| Number of Processes / Cores | Sequential (-O2) |  SIMD (AVX2, -O2) | MPI (-O2)  | Pthread (-O2) | OpenMP (-O2) | CUDA | OpenACC |
|-----------------------------|------------------|-------------------|------------|---------------|--------------|------|---------|
| 1                           | 3745             | 3856              | 3670       | 3663          | 3673         | 9.70861 | 5      |
| 2                           | N/A              | N/A               | 2840       | 2799          | 2785         | N/A  | N/A     |
| 4                           | N/A              | N/A               | 1431       | 1450          | 1455         | N/A  | N/A     |
| 8                           | N/A              | N/A               | 723        | 857           | 731          | N/A  | N/A     |
| 16                          | N/A              | N/A               | 360        | 377           | 453          | N/A  | N/A     |
| 32                          | N/A              | N/A               | 185        | 264           | 265          | N/A  | N/A     |
