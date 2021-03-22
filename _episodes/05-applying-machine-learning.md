---
title: "Applying Machine learning"
teaching: 0
exercises: 0
questions:
- "What are the essential steps for developing a machine learning project?"
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

## Predictions into actions

Machine learning models produce predictions. We can use these predictions in a variety of ways. How we use these predictions is a critical consideration when using Machine Learning. A “perfect” model could be useless if the predictions it makes are used in an inappropriate way and an “average” model might be beneficial if it is carefully used within other workflows. 

Let’s look at an example to illustrate the predictions generated by a machine learning model can be used very differently. For our example, we’ll consider a machine learning model that takes some text as input and predicts the language of that text.  The predictions generated by this model could be used:

- To directly create metadata for the language field for an item.
- To show the language code as a suggestion to a human cataloguer who can choose to use or ignore the suggestion.
- To directly create the language code for a record if the model ‘confidence’ is above a certain level, and show it to a human cataloguer if the prediction falls below a confidence threshold.
- Show the predicted language and confidence score to the user of a public catalogue system with a button allowing the user to indicate if they think the prediction is correct or not. 

You can hopefully see from these examples that there are many potential ways to utilise the predictions made by a machine learning model. The way in which you decide to use the predictions of a model will depend on many factors; existing infrastructure, staff attitudes towards machine learning, user needs etc. 

\ # TODO Add exercise here on how to make use of predictions based on what is covered in previous lessons?

## People and Skill 

You will need the right might mix of people and skills to successfully apply machine learning in a GLAM setting. 

> ## Identifying skills required for a machine learning project
>
> - What are some of the skills you think you might need for completing an Machine Learning project?  
> - Where might you find these skills in your organization?
>
> > ## Skills which are likely to be important
> >
> > - Domain expertise: it is important that people with intimate knowledge of the collections or ‘business’ need to be addressed are involved in the development of machine learning approaches. 
>> - Project management: to keep track of progress
>> - IT: if you are going to work with existing infrastructure you might need support from IT for things like the storage of data
>> - Communication skills: to communicate the goals of the project internally and potentially to external audiences
>> - Team working skills: it is likely that most machine learning projects done in a GLAM setting will be done as part of a team
> >
> {: .solution}
{: .challenge}

You will probably notice that there are many skills that are likely to be important for the success of a project beyond direct data science or coding skills. We will look more closely at these data science skills later in this episode. 

## Data 
As we saw in the previous episode data is of central importance for developing Machine Learning models. The process involved in preparing data for use in a machine learning project will depend on what you are trying to achieve, the kind of machine learning you want to use but there are some broad considerations that will apply in many situations. 

\ # TODO see where this data section fits in relation to the previous episodes 
?Maybe: Creating a smallish set for testing external methods
?Maybe: Creating a small test for the initial model training to establish feasibility 


