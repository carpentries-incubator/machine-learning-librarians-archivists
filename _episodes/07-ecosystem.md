---
title: "The Machine Learning ecosystem"
teaching: 0
exercises: 0
questions:
- FIXME
objectives:
- FIXME
keypoints:
- FIXME
---
FIXME

{% include links.md %}

## Episode Introduction





## Sharing what you have developed/learned 

**Training Data** 
\ # TODO possibly chop if covered elsewhere 
  - **Why?**:
    - Training data is time-consuming to produce and others may be able to reuse or build on your data
    - Being able to interrogate the data used to train a model may help give insights into the limitations of any models based on this data
    - Having shared datasets makes it easier for people to establish what is reasonable performance to expect for a particular model/task because they can compare results. 
  - **Possible approach?**
    - Share in an existing data repository
    - Include a clear license to indicate terms of use
    - Include documentation about how the dataset was constructed. [*Datasheets for datasets*](https://arxiv.org/abs/1803.09010f) offers a useful template for approaching this documentation.  

**Models**
  - **Why?**
    - It is likely that a lot of work went into creating this model and it is possible others could also benefit from this model 
    - Training some machine learning models has a large environmental impact. Sharing models can help this environmental cost being occurred multiple times.  
  - **Possible approach?**
    - Depending on how you are using your model’s predictions the model itself might be contained inside an ‘application’. This application could be shared directly or you might decide to share the model weights. 
    - It is important to document your model. The original intended use, limitations and a link to the training data will all help enabel people to evaluate how they could use your model. [*Model Cards for Model Reporting*](https://arxiv.org/ct?url=https%3A%2F%2Fdx.doi.org%2F10.1145%2F3287560.3287596&v=b782538f) provides guidance for what this documentation should include. 

**Processes, successes and failures** beyond sharing the more tangible outcomes of a machine learning project documenting the broader project will help other GLAM institutions apply machine learning. This documentation could include;
- The problem you were trying to solve
- Alternatives to machine learning considered
- How you created your training data
- The metrics which were important to you
- The models you considered
- The experiments you ran and the results of those experiments

There are various ways in which this work can be documented. Academic papers are a possible avenue for sharing the results of experiments but should not be considered as the ‘sole’ medium for sharing meaningful work. The format of many academic journals is likely to preclude sharing ‘failed’ projects and it may be challenging to publish more ‘modest’ uses of machine learning because they are deemed to lack ‘novelty’.

Beyond academic papers, there are a growing number of tools for managing machine learning projects which include data versioning, experiment tracking and other features for documenting work. Public version control repository like GitHub or GitLab offer venus for sharing code and you may explore using other tools like Jupyter notebooks to help make your models more accessible to others. 

>## Resources Consulted & Recommended Reading
>
> - Ameisen, Emmanuel. Building Machine Learning Powered Applications: Going from Idea to Product, 2020.
> - Cordell, Ryan. ‘Machine Learning + Libraries’. LC Labs. Accessed 28 March 2021. <https://labs.loc.gov/static/labs/work/reports/Cordell-LOC-ML-report.pdf>.
> - Gebru, Timnit, Jamie Morgenstern, Briana Vecchione, Jennifer Wortman Vaughan, Hanna Wallach, Hal Daumé III, and Kate Crawford. ‘Datasheets for Datasets’. ArXiv:1803.09010 [Cs], 19 March 2020. <http://arxiv.org/abs/1803.09010>.
> - Howard, Jeremy, Sylvain Gugger, and an O’Reilly Media Company Safari. Deep Learning for Coders with Fastai and PyTorch, 2020.
> - Lakshmanan, Valliappa, Sara Robinson, Michael Munn, and an O’Reilly Media Company Safari. Machine Learning Design Patterns, 2021.
> - Mitchell, Margaret, Simone Wu, Andrew Zaldivar, Parker Barnes, Lucy Vasserman, Ben Hutchinson, Elena Spitzer, Inioluwa Deborah Raji, and Timnit Gebru. ‘Model Cards for Model Reporting’. Proceedings of the Conference on Fairness, Accountability, and Transparency, 29 January 2019, 220–29. <https://doi.org/10.1145/3287560.3287596>.
> - Padilla, Thomas. ‘Responsible Operations: Data Science, Machine Learning, and AI in Libraries’. OCLC, 26 August 2020. <https://www.oclc.org/research/publications/2019/oclcresearch-responsible-operations-data-science-machine-learning-ai.html>.
> - Slee, Tom. ‘The Incompatible Incentives of Private Sector AI’. Tom Slee, 31 March 2019. <https://tomslee.github.io/publication/oup_private_sector_ai/>.
> - Suresh, Harini, and John V. Guttag. ‘A Framework for Understanding Unintended Consequences of Machine Learning’. ArXiv:1901.10002 [Cs, Stat], 17 February 2020. <http://arxiv.org/abs/1901.10002>.
> - Omoju Miller. ‘The Myth of Innate Ability in Tech’. Accessed 20 March 2021. <http://omojumiller.com/articles/The-Myth-Of-Innate-Ability-In-Tech>.
> - Thomas, Rachel. ‘The Problem with Metrics Is a Big Problem for AI · Fast.Ai’. fast.ai blog. Accessed 18 March 2021. <https://www.fast.ai/2019/09/24/metrics/>.

{: .checklist }
