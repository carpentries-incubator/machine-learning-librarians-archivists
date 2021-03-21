---
title: "Applying Machine learning"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---
FIXME

{% include links.md %}

## Applying Machine learning
In this episode, we turn to the question of how we can apply machine learning in a GLAM setting.  We’ll move through the process of applying machine learning step-by-step to make these stages easier to follow. In reality, this process will rarely be completely linear and you likely need to iterate on many steps of the process. 

## Machine Learning projects 
A report has suggested that 85% of AI projects “ultimately fail to deliver on their intended promises to business”. Successfully applying machine learning in a GLAM setting involves a range of challenges including; data quality, identifying ethical concerns building or adapting machine learning models, internal and external communication. 


> ## What does failure mean in your institution
>
> What do you think is the most likely reason an ML project would ‘fail’ in your institution. What would ‘failing’ mean?
{: .discussion}


\ # TODO illustration of the overall steps of ml application pipeline?


## What is the "business" need?


There are many possible uses of Machine Learning in a GLAM context. These can range from projects with a relatively limited scope to ambitious “end-to-end” applications of Machine Learning across core infrastructure.

It is important that you have a clear idea of what your goal is in applying Machine Learning. This could be a relatively open-ended goal of ‘exploring what might be possible but sometimes you will have a much more concrete outcome you are hoping to achieve. Some example of business needs that could potentially be addressed using Machine Learning: 

| Type of use case                                                       | GLAM Example                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Using Machine learning to help address an existing ‘problem’           | You use an external API service to produce OCR for digitised material in your collection. This service charges per image submitted. You know you are currently submitting many pages to this service where there is no text on the page. This means you are spending additional money on this service. The volume of images makes it hard to manually check for blank pages. Ideally, you want some kind of system that can filter out these images so they aren’t submitted to the OCR service.  |
| Using Machine learning to enable new ways of working with a collection | Your institution has a large collection of digitised newspapers. Some of these newspapers included illustrations of various kinds. At the moment the only way these images can be found by browsing through images one at a time. You would love to be able to identify where these images are in the collection without having to look through millions of pages manually.                                                                                                                       |
| Using Machine learning to make connections                             | Your institution has a range of collections that have been digitised but don’t contain much metadata. You think that exposing some key information from unstructured text documents may help users search and explore these collections.                                                                                                                                                                                                                                                          |
| Using Machine learning to explore new research questions               | You have collections of materials that are too large to explore individually. You think that interesting trends might be found by exploring these collections at scale. You have previously used n-grams to explore the usage of words over time but you think that developments in Natural Language Processing using machine learning might enable new questions to be explored.                                                                                                                 |


> ## Use cases for Machine Learning in your Organization
>
> Where do you think ml could be used in your organization? 
> Would machine learning be used to do something new or help with existing processes or systems?
{: .discussion}

