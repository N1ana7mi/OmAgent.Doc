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

## Training two layer neural network 400 hidden units

| Epoch | Acc Rate | Training Time (Sequential (Optimized with -O2))| Training Time (OpenACC kernel)| Training Time (OpenACC fusion) |
|-------|----------|---------------|---------------|---------------|
|     1 |   92.330%  |  47273 ms  |   8353 ms  |   4878 ms  | 
|     2 |   93.960%  | 47278 ms  |   7148 ms  |   4770 ms  | 
|     3 |   94.980%  | 47278 ms  |   7164 ms  |   4777 ms  | 
|     4 |   95.720%  | 47266 ms  |   7196 ms  |   4827 ms  | 
|     5 |   96.320%  | 47200 ms  |   7211 ms  |   4839 ms  |
|     6 |   96.560%  | 47257 ms  |   7245 ms  |   4867 ms  |  
|     7 |   96.880%  | 47212 ms  |   7245 ms  |   4869 ms  | 
|     8 |   97.110%  | 47231 ms  |   7296 ms  |   4911 ms  | 
|     9 |   97.280%  | 47247 ms  |   7317 ms  |   4923 ms  | 
|    10 |   97.410%  |  47193 ms  |   7320 ms  |   4924 ms  | 
| Total Execution Time: |  / | 517873ms   |   75654 ms  |   50547 ms   |    
| Speed up (Sequential base) |    /  |  1  | 0.146  |  0.097  |

## PartB
| Number of Processes / Cores | Sequential | SIMD (AVX2) | MPI  | Pthread | OpenMP | CUDA | OpenACC |
|-----------------------------|------------|-------------|------|---------|--------|------|---------|
| 1                           | 6642       | 4239        | 7222 | 8036    | 8468   | 31.1593   | 23      |
| 2                           | N/A        | N/A         | 7081 | 7217    | 7296   | N/A  | N/A     |
| 4                           | N/A        | N/A         | 3734 | 3825    | 3938   | N/A  | N/A     |
| 8                           | N/A        | N/A         | 2076 | 1829    | 1893   | N/A  | N/A     |
| 16                          | N/A        | N/A         | 1057 | 950     | 965   | N/A  | N/A     |
| 32                          | N/A        | N/A         | 655  | 564     | 588    | N/A  | N/A     |




## PartC
| Number of Processes / Cores | Sequential (SOA，-O2) |  SIMD (AVX2, -O2) | MPI (-O2)  | Pthread (-O2) | OpenMP (-O2) | CUDA | OpenACC |
|-----------------------------|------------------|-------------------|------------|---------------|--------------|------|---------|
| 1                           | 1             | 1.058              | 1.006       | 1.004          | 1.007         | 0.002 | 0.001      |
| 2                           | N/A              | N/A               | 0.779       | 0.768          | 0.764         | N/A  | N/A     |
| 4                           | N/A              | N/A               | 0.392       | 0.398          | 0.399         | N/A  | N/A     |
| 8                           | N/A              | N/A               | 0.198        | 0.235           | 0.200          | N/A  | N/A     |
| 16                          | N/A              | N/A               | 0.099        | 0.103           | 0.124          | N/A  | N/A     |
| 32                          | N/A              | N/A               | 0.050        | 0.072           | 0.073          | N/A  | N/A     |
