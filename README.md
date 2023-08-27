# Computational Psychiatry in Post-Traumatic Stress Disorder (PTSD)

In this project, we aimed to achieve a greater understanding of the landscape of computational psychiatry in PTSD and demonstrate a common practice of computational modelling in psychiatric research.

We first explored the concepts in computational psychiatry in a general sense and the dominant hypothesis of PTSD: (1) abnormal fear learning and (2) exaggerated threat detection. Recent computational studies have used reinforcement learning (RL) models to fit behavioural experiments with PTSD patients. We exhaustively described three model-free RL: (1) Rescorla-Wagner (RW) model, (2) Pearce-Hall (PH) model and (3) Gain-loss model and one model-based RL: latent-state (LS) model. Besides, we discussed the distinctions between these computational models of PTSD. By investigating the current papers on PTSD, which use the quantitative abductive approach of computational psychiatry, we also discussed the research findings obtained using these models. 

To demonstrate a common practice of computational modelling in psychiatric research, we implemented the RW model in Python from scratch accordingly to the imaginary experiment by following Wilson et al.’s guideline[87]. We use the implemented RW model to generate artificial data. Through simulation, we ensure the RW model captures the learning behaviours that the experiment intends to generate and hypothesise that the PTSD participants might assign more weight to the prediction error. 

<img width="613" alt="data_simulation_graph" src="https://github.com/abc12345d/Markdown_workspace/assets/44512722/5a7d18d6-d152-495a-b052-5eb681062247">

By running a successful parameter recovery on the artificial data (see below figure), we increase the validity of the best-fitting parameter values in describing the real behavioural data. The RW model can then be fitted to behavioural data collected from the real experiment, and the best-fitting parameter values can potentially function as an indicator of PTSD. This is the approach used in Homan et al.’s study. From there, they fitted the RW model to real SCR data from trials of the healthy control group and PTSD patient group. They then analysed the model parameters to find out if there were any statistical differences between the two groups. 

<img width="553" alt="simulated_lr_vs_recovered_lr" src="https://github.com/abc12345d/Markdown_workspace/assets/44512722/927b7fcc-b2fd-413f-9697-827ef3c650cb">

Traceplot for sampling 4 runs of MCMC for 1_000 tune and 1_000 draw iterations:
The left column consists of a smoothed histogram (using kernel density estimation) of the marginal posteriors of each stochastic random variable while the right column contains the samples of the Markov chain plotted in sequential order. 

<img width="746" alt="mcmc_result" src="https://github.com/abc12345d/Markdown_workspace/assets/44512722/1ee8b0db-e67f-4b77-a4c8-551ffb2dfc70">
