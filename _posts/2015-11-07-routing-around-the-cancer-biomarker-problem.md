---
layout: tag_post
title: Routing Around The Cancer Biomarker Problem With Antibodies
tags: [cancer, medicine, lit-review]
---

One of the heuristics I’ve been using in this series is that drugs that rely on tumor-specific biomarkers are not very effective. We’ve seen that most targeted chemotherapies have little or no effect on survival; we’ve seen that immunotherapies that depend on tumor-specific antigens are limited by the tendency of advanced cancers to “escape” immunosurveillance by shedding their antigens.

The “cancer is hard and complex” model accurately predicts this. Cancer is diverse, both between tumor types and across the course of the disease.  Most tumor-specific biomarkers also occur on some healthy tissues, and _don’t_ occur on all tumors.  Most targeted drugs have problems with both _sensitivity _and _specificity_ — they miss too many cancer cells, and attack too many healthy cells.

But cancer might _not_ be as hard if you can _route around the complexity_ by focusing on vulnerabilities that all or most cancers have in common.

[This paper](http://www.nature.com/articles/srep05088) from a team of researchers led by Sanford Simon provides one possible strategy: detecting endogenous antibodies.

Specific autoantibodies to particular tumor-specific antigens have fairly low sensitivity for cancer. For example, “In patients with hepatocellular carcinoma (HCC), probing for a single autoantibody in the serum gives a positive result in 10–20% of patients; the detection increases to 66% with a panel of ten autoantibodies[2](http://www.nature.com/articles/srep05088#ref20)0. While the sensitivity of tumor detection can be increased by using a panel of antibodies over a single antibody[21](http://www.nature.com/articles/srep05088#ref21), the results are still insufficient for diagnosis in many tumor types.”

Antibodies are part of the adaptive immune response. Also known as immunoglobulins, they are Y-shaped molecules produced by B cells that tag microbes, infected cells, or tumor cells for further attack by other parts of the immune system.

What if, instead of trying to detect a tumor-specific antigen with a targeted drug, you tried to detect _all_ the tumor-specific antigens at once by detecting all the _antibodies_ that the body is already using to identify tumor cells?

That’s what Simon and his team did. They attached a fluorescent chemical to an anti-IgG antibody, which binds to _all_ IgG antibodies (regardless of which antibody they’re selecting for.) The fluorescence was 64x greater in mouse tumor tissue than in normal tissue.

The effect worked across a wide variety of mouse  cancer types: breast cancer, prostate cancer, liver cancer, leukemia, etc.

IgG autoantibodies are [abundant ](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0060726)in all human, rat, and swine sera, increase with age, and are statistically significantly lower in cancer, Alzheimer’s, and Parkinson’s patients compared to age- and gender-matched controls; they are hypothesized to play a role in clearing the body of debris and damaged or mutated cells.

[Gold nanoparticles ](http://pubs.acs.org/doi/abs/10.1021/acsami.5b00371) mixed with blood serum pick up a “corona” of protein which includes IgG molecules of all types, and the total amount of IgG is higher in cancer than non-cancer patients.  “The test has a 90–95% specificity and 50% sensitivity in detecting early stage prostate cancer, representing a significant improvement over the current PSA test.”

I’ve spoken to Dr. Simon and seen some of his unpublished results, which involved distinguishing tumor from healthy tissue down to the cellular level with fluorescent anti-IgG, in both mice and human tumors of many types.

In a sense, this is an “obvious” idea. If the body produces many kinds of tumor-specific antibodies, each of which selects for _some_ cancers_, _then measuring the _overall _level of _all_ antibodies would be a much more robust test that selects more specifically for a wider range of cancers.  It’s essentially just [bagging](https://en.wikipedia.org/wiki/Bootstrap_aggregating) applied to cancer detection.

This is usually presented as a method for _detecting_ cancer, but it could also be a method for _treating_ cancer.  Attaching cytotoxic chemotherapy to an anti-IgG antibody (in place of the fluorescent protein) would concentrate the chemo in the tumor as opposed to the rest of the body, allowing higher doses to be administered safely.

It could also be a guide for better cancer surgery; washing the body cavity with IgG-binding fluorescent protein would make the tumor area light up, helping the surgeon cut precisely where needed and making sure to get adequate margins.

Obviously much more development is needed to identify exactly how precise anti-IgG is on humans.  Since cancers eventually lose antigens as they advance, this can be expected to be less effective on advanced cancers.  However, since cancers lose antigens _one at a time_ as they mutate, an anti-IgG-based therapy that was sensitive to _all_ antigens at once would in principle lose effectiveness later than an immunotherapy based only on a single antigen.

As far as cancer heuristics go, IgG detection is definitely “simple”, it is fairly “upstream”, but it is only moderately “decisive” (we don’t yet have extended survival times or extremely high published precision numbers).  I think it’s potentially important and under-appreciated, however, especially given the very _high_ level of current investment in antibody-based immunotherapies.

