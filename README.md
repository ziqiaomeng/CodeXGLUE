# Introduction

According to [Evans Data Corporation](https://evansdata.com/press/viewRelease.php?pressID=278), there are 23.9 million professional developers in 2019, and the population is expected to reach 28.7 million in 2024. With the growing population of developers, code intelligence, which aims to leverage AI to help software developers improve the productivity of the development process, is growing increasingly important in both communities of software engineering and artificial intelligence. 

When developers want to find code written by others with the same intent, [code search](https://arxiv.org/abs/1909.09436) systems can help automatically retrieve semantically relevant code given natural language queries. When developers are confused about what to write next, [code completion](https://arxiv.org/abs/1912.00742) systems can help by automatically completing the following tokens given the context of the edits being made. When developers want to implement Java code with the same function of some existing body of Python code, [code-to-code translation](https://arxiv.org/abs/2006.03511) systems can help translate from one programming language (Python) to another (Java). 

Code intelligence therefore plays a vital role in Microsoft’s mission to empower developers. As highlighted by Microsoft CEO Satya Nadella at Microsoft [Build 2020](https://mybuild.microsoft.com/sessions/23912de2-1531-4684-b85a-d57ac30af09e), the role of developers is more important than ever. GitHub is increasingly the default home for source code, and Visual Studio Code is the most popular code editor. Microsoft offers the most complete toolchain for developers, bringing together the best of GitHub, Visual Studio, and Microsoft Azure to help developers to go from idea to code and code to cloud. 

Recent years have seen a surge of applying of statistical models, including neural nets, to code intelligence tasks. Very recently, pre-trained models learned from big programming language data  have been inspired by the great success of large pre-trained models like [BERT](https://arxiv.org/abs/1810.04805) and [GPT](https://arxiv.org/abs/1908.09203) in natural language processing (NLP). These models, including [IntelliCode](https://arxiv.org/pdf/2005.08025.pdf) and [CodeBERT](https://arxiv.org/pdf/2002.08155.pdf), obtain further improvements on code understanding and generation problems. However, the area of code intelligence lacks a benchmark suite that covers a wide range of tasks. We have seen that a diversified benchmark dataset is significant for the growth of an area of applied AI research, like [ImageNet](http://image-net.org/) for computer vision and [GLUE](https://gluebenchmark.com/) for NLP. 

To address this, researchers from Microsoft Research Asia, Developer Division, and Bing introduce CodeXGLUE, a benchmark dataset and open challenge for code intelligence. It includes a collection of code intelligence tasks and a platform for model evaluation and comparison. CodeXGLUE stands for General Language Understanding Evaluation benchmark for CODE. It includes 14 datasets for 10 diversified code intelligence tasks covering the following scenarios: 

*	**[code-code](https://github.com/microsoft/CodeXGLUE/tree/main/Code-Code)** (clone detection, defect detection, cloze test, code completion, code refinement, and code-to-code translation)
* **[text-code](https://github.com/microsoft/CodeXGLUE/tree/main/Text-Code)** (natural language code search, text-to-code generation) 
* **[code-text](https://github.com/microsoft/CodeXGLUE/tree/main/Code-Text/)** (code summarization) 
* **[text-text](https://github.com/microsoft/CodeXGLUE/tree/main/Text-Text)** (documentation translation) 

A brief summary of CodeXGLUE is given below, including tasks, datasets, language, sizes in various states, baseline systems, providers, and short definitions of each task. Datasets highlighted in BLUE are newly introduced. 
![avatar](https://uc66743fa042b33be6a5f8751b7a.previews.dropboxusercontent.com/p/thumb/AA7p-u2Sh3UZmRW2o1RAtKAM5cSK-sp6ezfrzBwSHT8Av3w8zEd1Ye8NvFB4T0pl-Je50wsDJ-9ZXy5SvvxF8a_fUGPt9TQrYHa5ndIxpVJtlYesaBTOZKh7QVeM2MRjU5LzbiLC0TZkOScg1uY_uvHdBvuK1LEOY4qgxwHV9gTRECrPgmxHrkpwdf0dZPKlPqBWyTJM4OCIB2QpNDQtc6fOTKB4XhBnNTPugEyePDTqiWTcrKmz7uVfY9rHgNsdGuCKvkGHYLhgflrXu7h1EDTnqTIvjH5QcyWIaa9s8s1nvcOw212Iq7SfJnqiB72r2Hp-yZfLGZ55nc998__cO6wmPaC8lBeBk6xSmm9hAcVLymdx66rovBWBDIcVxXqfr4JHNr7TmhGpXcI0XNjR-H8h/p.jpeg?fv_content=true&size_mode=5)



To make it easy for participants, we provide three baseline models to support these tasks, including a BERT-style pre-trained model (in this case, CodeBERT), which is good at understanding problems. We also include a GPT-style pre-trained model, which we call CodeGPT, to support completion and generation problems. Finally, we include an Encoder-Decoder framework that supports sequence-to-sequence generation problems.

Three pipelines including CodeBERT, CodeGPT, and Encoder-Decoder are provided to make it easy for participants.
![avatar](https://uc719a554a8036546eb8129862cb.previews.dropboxusercontent.com/p/thumb/AA6654nQpuvSGaLUuAhLT3BVBI1ZER0JDJpxW4nsSMsz2Z6i3gq6eaTW8GA5Pb6jHAhH1Xoz-3ui2nhCqBqTWZzHNffFfBkrF7KdnZpWQgYrrrpsKEnsBgO9qFRjfjcFySXCn0RURELAhGH-ReHIy5b9MuOxn0y1oJ8GVmuKQX88o6uOUXIAtJVfYD2kS42HM1gdZF8pC1Ou3X_okbltKgTcEC6sG6PU2Rr1ObTUXEebJ4yQMAdKQXLbjR8b6fK_Y20ihS3YbREMULWyDhxqAYYZaCOaD4P8rfk6V55lCpWmPfKsIHuWFzl4dvaKlCSIeu5820mf1Hi_w4kMCdS23M7CqPQsqhhgmF56FDG6OFmPGUCrEy8HcBz3c9SEatnlxF3AUqGG4wBRX7flkWAzpBf7/p.jpeg?fv_content=true&size_mode=5)


With CodeXGLUE, we seek to support the development of models that can be applied to various code intelligence problems, with the goal of increasing the productivity of software developers. We encourage researchers to participate in the open challenges to continue progress in code intelligence. Moving forward, we’ll extend CodeXGLUE to more programming languages and downstream tasks while continuing to push forward pre-trained models by exploring new model structures, introducing new pre-training tasks, using different types of data, and more.

# Relevant Links
[Leaderboard](https://microsoft.github.io/CodeXGLUE/) | CodeXGLUE paper (coming soon)

# Tasks and Datasets

Below, we elaborate on the task definition for each task and newly introduced datasets that are highlighted in the table above.

1.	Clone detection (BigCloneBench, POJ-104). A model is tasked with measure the semantic similarity between codes. Two existing datasets are included. One is for binary classification between code and the other is for retrieving semantically similar code given code as the query. 

2.	Defect detection (Defects4J). A model is tasked with identifying whether a body of source code contains defects that may be used to attack software systems, such as resource leaks, use-after-free vulnerabilities and DoS attack. An existing dataset is included.

3.	Cloze test (CT-all, CT-max/min). A model is tasked with predicting the masked token from  code, formulated as a multi-choice classification problem. The two datasets are newly created, one with candidates from the (filtered) vocabulary and the other with candidates among “max” and “min”.
 
4.	Code completion (PY150, GitHub Java Corpus). A model is tasked with predicting following tokens given a code context. Both token-level and line-level completion are covered. The token-level task is analogous to language modeling, and we include two influential datasets here. Line-level datasets are newly created to test a model’s ability to autocomplete a line. 

5.	Code translation (CodeTrans). A model is tasked with translating the code in one programming language to the code in another one. A dataset between Java and C# is newly created.

6.	Code search (CodeSearchNet, AdvTest; StacQC, WebQueryTest). ). A model is given the task of  measuring  semantic similarity between text and code. In the retrieval scenario, a test set is newly created where function names and variables in test sets are replaced to test the generalization ability of a model. In text-code classification scenario, a test set where natural language queries come from Bing query log is created to test on real user queries.

7.	Code refinement (Bugs2Fix). A model is tasked with trying to automatically refine the code, which could be buggy or complex. An existing dataset is included.

8.	Text-to-code generation (CONCODE). A model is given the task to generate code given natural language description. An existing dataset is included.

9.	Code summarization (CodeSearchNet). A model is given the task to generate natural language comments for a code. Existing datasets are included.
  
10.	Documentation translation (Microsoft Docs). A model is given the task to translate code documentation between human languages. A dataset, focusing on low-resource multilingual translation, is newly created.

# Training and Inference Time Cost
We calculate the training and inference time cost for each dataset with 2 P100 GPUs. Results are shared in the following table.
![avatar](https://uc6aeaa7555a6c864fd3006e4d37.previews.dropboxusercontent.com/p/thumb/AA78rIL_AMPfwysYQW7mlRw0qPLnWN_wwh3-9RGDaCDFpnc7KZG0miZhQg6MXTR601U64wrBZWb2oNcxWYXJXa4agpZMb8sSyGqavBzfJTQFiE9NdP98FOWNgS2P_TsgNgcWr37r1KVtDY1Pfs4fY3j0Yu0XQ0hXHo_hh1gqJ8ruVBqM9_mN-nTCwwiAUi6p_MAIJc50skHdUhVpc0GQHegX5bYiRtysgefbYHjBrj0i7nS8aoDBj7Pqm-60YDWufHEyG-Fhb4cqA1-jhuAxzAowrPtYkPpRuh--SaL_O_S7wIn6keqaFJrB063Cz7V3JuCcydcK9SHh5qUV3ZU_XoGyBNL8jFxBYP9kE6GbyvH5ibLUOs3JWtzqb8uz_J9hFvTV1CWBpbSPi-Egs9fo29DX/p.jpeg?fv_content=true&size_mode=5)

# LICENSE
Our codes follow MIT License.

Our datasets follow Computational Use of Data Agreement (C-UDA) License.

# Reference
If you use this code or CodeXGLUE, please consider citing us.
<pre><code>@article{CodeXGLUE,
  title={CodeXGLUE: A Benchmark Dataset and Open Challenge for Code Intelligence},
  year={2020},
}</code></pre>

This research was conducted by Alexey Svyatkovskiy, Ambrosio Blanco, Colin Clement, Dawn Drain, Daxin Jiang, Daya Guo, Duyu Tang, Junjie Huang, Lidong Zhou, Linjun Shou, Long Zhou, Michele Tufano, Ming Gong, Ming Zhou, Nan Duan, Neel Sundaresan, Shao Kun Deng, Shengyu Fu, Shuai Lu, Shujie Liu, and Shuo Ren.
