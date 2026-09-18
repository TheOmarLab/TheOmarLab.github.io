---
title: Research in the Omar Lab
layout: default
group: research
description: "Our research focuses on AI-powered multimodal risk stratification, digital pathology, and tumor microenvironment analysis for cancer patients at Cedars-Sinai."
---

<div class="row">

# Our research
We build artificial intelligence (AI) tools that read tissue the way biology is organized, so that predictions about a patient's disease rest on interpretable structure rather than opaque correlations. Our models are trained with the composition of the tumor microenvironment (TME) in the loop, which makes them more robust, easier to interrogate, and more likely to hold up in cohorts they were never trained on. We work across transcriptomics, spatial omics, histopathology, and radiology, and we ask the same question of every modality: what is the tissue actually doing, and what does that imply for the patient in front of us?

#### Our work focuses mainly on prostate cancer; however, it is important to note that our approaches can be applied to other cancer types as well  
<br>
<br>

</div>

<div class="row">

### Identifying digital pathology signatures of high-risk cancer phenotypes

<div class="col-md-7 order-md-1 align-self-center">

We are interested in uncovering pathomic signatures from routine H&E-stained whole slide images (WSIs) to inform patients' prognostication and the prediction of molecular and clinical phenotypes (see [Omar et al. Ann Rev of Cancer Bio. 2024](https://www.annualreviews.org/content/journals/10.1146/annurev-cancerbio-062822-010523)).
Our work in this domain leverages deep learning algorithms to automate WSIs preprocessing and feature extraction to identify morphometric features associated with certain phenotypes. For instance, we developed a robust model for inferring the status of TMPRSS2:ERG fusion (a key molecular alteration in prostate cancer) from the tissue morphology depicted in routine H&E-stained images of radical prostatectomy specimens (see [Omar et al. Mol Cancer Res 2024](https://aacrjournals.org/mcr/article/22/4/347/741845/Semi-Supervised-Attention-Based-Deep-Learning-for)).
More recently, we asked whether tissue architecture alone carries prognostic signal when the model never sees outcome during training, and found that an outcome-blind architecture score is associated with prostate cancer-specific mortality (see [Lê et al. 2026](https://www.researchsquare.com/article/rs-10990195/v1)).

</div>
<div class="col-md-5 order-md-2 align-self-center d-flex justify-content-center">
<img class="img-fluid" style="max-height: 460px; width: auto;" src="/static/img/pub/erg.jpeg" alt="ERGmodel" loading="lazy">
</div>
</div>

<div class="row">

### Measuring how tissue responds to treatment over time

<div class="col-md-7 order-md-2 align-self-center">

When a patient is biopsied before and during treatment, an apparent change in a cell population can mean several different things: the cells may be doing something different, they may be present in different proportions, or the tissue may simply have been sampled or dissociated differently. Conflating these leads to confident conclusions that do not replicate.

We develop participant-level statistical methods for longitudinal single-cell and spatial experiments that treat the participant, not the cell, as the biological replicate, and that separate molecular activity from population representation while carrying the uncertainty of the measurement itself. A parallel line of work asks the same question of tissue organization: whether the spatial arrangement of a tissue has changed beyond what shifts in cell density and geometry would already explain. These methods are released as open software (see [sctrial](https://www.omar-lab.com/sctrial/)).

</div>
<div class="col-md-5 order-md-1 align-self-center">
<img class="img-fluid" src="/static/img/research/longitudinal_response.png" alt="Participant-level analysis of longitudinal tissue responses" loading="lazy">

</div>
</div>

<div class="row">

### Building multimodal risk stratification tools for clinical decision making

<div class="col-md-7 order-md-1 align-self-center">

Our lab develops multimodal risk stratification tools that integrate diverse patient-centered data types, including omics, pathomics, and radiomics, to sharpen risk assessment and inform patient management.
Omics offer a deep dive into the molecular underpinnings of tumor progression, while pathomics provide a spatial microscopic view of TME dynamics by translating pathology images into quantifiable data. Radiomics further enrich this by extracting non-invasive macroscopic features from medical imaging that can be correlated with underlying disease mechanisms and outcomes. Rather than concatenating these modalities and hoping a model finds the signal, we use TME-derived biology to constrain which features each encoder is allowed to rely on, so the resulting risk estimate is traceable to tissue state. Our goal is a decision point clinicians actually face: after a diagnostic biopsy, which patients need treatment intensification, and which can be safely watched.

</div>
<div class="col-md-5 order-md-2 align-self-center d-flex justify-content-center">
<img class="img-fluid" src="/static/img/research/multimodal_framework.png" alt="Biology-guided multimodal framework for post-biopsy prostate cancer risk assessment" loading="lazy">
</div>
</div>

<div class="row">

### Forecasting tissue adaptation

<div class="col-md-7 order-md-2 align-self-center">

Tumors do not sit still under therapy; they adapt, and the tissue reorganizes around them. The long-term ambition of the lab is to move from describing that adaptation after the fact to forecasting it: given the state of a tissue now, which trajectory is it on, and what would change it? This requires representations that are stable enough to compare across time points and biologically grounded enough to be acted on, which is why tissue modules, longitudinal inference, and multimodal integration are pursued as one program. The approach is disease-agnostic, and we develop it in prostate cancer because the natural history, sampling, and outcome data are rich enough to test it.

</div>
<div class="col-md-5 order-md-1 align-self-center">
<img class="img-fluid" src="/static/img/pub/digitalpath.gif" alt="digitalPath" loading="lazy">

</div>
</div>

