---
title: "Managing data bias"
teaching: 0
exercises: 0
questions:
- "How does dataset collection and construction affect models?"
- "What are common examples and definitions of bias in Machine Learning?"
- "How can we manage bias? Some lessons from GLAM"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---
FIXME

{% include links.md %}

## How does dataset collection and construction affect models?
Though AI and machine learning (ML) systems may appear to us as objective and neutral, dealing solely in facts and numbers and free of troublesome human weaknesses such as emotion in their decision making, in reality there are abundant opportunities for bias to enter ML systems at all stages of the pipeline: 

* ML systems fundamentally learn and make decisions based on the training data they are fed by us. If the data constructed is incomplete, or skewed in anyway, your model’s decisions will reflect this. 
* The decisions humans make when refining and reinforcing the models learning 
* The way in which the model is applied once built 

### Data is not neutral. 
The first thing to be aware of is that data is never neutral. In the simplest of terms, the very act of demarcating a chunk of data, no matter the size, for use in training a model exposes the fallacy that datasets can ever be neutral. A decision is always being made about what is included and what is not and those decisions can create bias whether intended or not. But more than this, data, as opposed to numbers, is about people.
> It’s all too easy to forget that data is about human beings and their behaviors. Data is not an abstraction….Data encodes the stories of our lives, capturing not only our tastes and interests but also our hopes and fears. Data isn’t an abstract idea or a set of numbers or qualitative responses. It can be and is, ultimately, human.
> 
Illustrative Example: 

### Collecting data indiscriminately vs curated sets
The manner in which data is typically sourced for training sets at the outset will have important implications on the model output. Because of the many complexities around copyright and licensing, privacy issues and high costs involved in sourcing access to large quality datasets, computer scientists have tended towards using what they can find freely, and indiscriminately, out in the wilds of the internet such as Wikipedia. 

Illustrative Example: ImageNet FlickR

### Annotating data
Bias can crop up in annotations made by humans either consciously or unconsciously. 

Illustrative Example: 

## Challenge
> Exercise: Annotate this image and compare your outputs with one other person. Differences?
{: .challenge}

### Applying ML systems 

[more on this]



It is imperative to be aware then that the manner in which data is collected, annotated and results applied, will have far reaching consequences for society as decisions produced by ML systems are increasingly being relied upon in real world scenarios. From seemingly benign systems like recommendation engines to predictive policing, opportunities for ML systems to perpetuate and amplify inequalities abound. Simply put: bias in….bias out. 

### Resources Consulted & Recommended Reading:
>
> - [Catanzaro, B. (2019, December 4). "Datasets make algorithms: how creating, curating, and distributing data creates modern AI." [Video file]. Retrieved from https://library.stanford.edu/projects/fantastic-futures] 
> - [Ekowo, M., 2016. Why Numbers can be Neutral but Data Can’t. [online] New America. Available at: <https://www.newamerica.org/education-policy/edcentral/numbers-can-neutral-data-cant/> [Accessed 23 March 2021]]
> - [Mayson, Sandra Gabriel, Bias In, Bias Out (September 28, 2018). 128 Yale Law Journal 2218 (2019), University of Georgia School of Law Legal Studies Research Paper No. 2018-35, Available at SSRN: https://ssrn.com/abstract=3257004]
> - [Padilla, T. (2019). Responsible Operations: Data Science, Machine Learning, and AI in Libraries. OCLC ResearchPosition Paper. https://doi.org/10.25333/xk7z-9g97 ]
{: .checklist }

## Common types of data bias

Let’s have a look at this riddle:

> ## Challenge: Consider this riddle 
>
> A father and son get in a car crash and are rushed to the hospital. The father dies. The boy is taken to the operating room and the surgeon says, “I can’t operate on this boy, because he’s my son.” How is this possible? 
>
>
> > ## Solution
> >
> > The surgeon is a woman. 
> > In research conducted on 197 BU psychology students (where women outnumbered men two-to-one) and 103 children, ages 7 to 17, only a small minority of subjects—15 percent of the children and 14 percent of the BU students—came up with this answer. Of self-described feminists in the student group, 78 percent did not guess the surgeon was the mother. 
> {: .solution}
{: .challenge}

The common definition of data bias is that the available data is not representative of the population or phenomenon of study. This may because the data does not include variables that properly capture the phenomenon we want to predict and/or includes content produced by humans which may contain bias against groups of people.

Let's look at some common types of bias that you may need to manage in the process of applying machine learning at your institution:

* Confirmation bias: 
* Correlation bias: 
* Selection bias: A data set overrepresents one certain group and underrepresents another. 
GLAM Example?: Existing metadata issues
* Prejudicial bias: A data set that incorporates data that the model should be ignorant of like a person’s race or gender
GLAM Example?: 
* Exclusion bias: Removing data from a set that we think isn’t relevant
GLAM Example?:
* Algorithmic bias: Unjust, unfair, or prejudicial treatment of people related to race, income, sexual orientation, religion, gender, and other characteristics historically associated with discrimination and marginalization, when and where they manifest in algorithmic systems or algorithmically aided decision-making
GLAM Example? 
* Modelling bias: bias introduced during the training process because of some decision made about what to optimize. For example we might aim to improve accuracy and are satisfied when we get to 90% accuracy. However this overall accuracy can hide that some particular ‘slices’ of our data might be doing much worse. A GLAM example of this could be using named entity recogntion accross multilingual newspapers. Your overall accruacy might be very good but your model may underperform on one language. This might not be addressed by changing your data but changing how you approach training/evaluating your model. 

Challenge: Look at an example table of data and think about what implicit information may be in it. What sorts of data contained within it could lead to bias issues? What types of bias issues? [will include answers]

Resource(s):

Rich, B., 2014. BU Research: A Riddle Reveals Depth of Gender Bias | BU Today | Boston University. [online] Boston University. Available at: <https://www.bu.edu/articles/2014/bu-research-riddle-reveals-the-depth-of-gender-bias/> [Accessed 22 March 2021].

## Lessons from GLAM: How can we manage bias?

Talk about why it’s important to manage bias, implications for institutions
 
Bit here about how as GLAM professionals managing bias is not a new concept, it’s baked into our experience of collection development.  
> Archives are the longest standing communal effort to gather human information and archive scholars have already developed the language and procedures to address and discuss many challenges pertaining to data collection such as consent, power, inclusivity, transparency, and ethics & privacy.
> 
Reference Lessons from archives: strategies for collecting sociocultural data in machine learning

* Enlist the help of staff with the right domain expertise to review your training data construction before and after, they may see biases that you have overlooked
* When collecting and annotating your data make sure to recruit diversified crowds for the task and carefully communicate instructions to manage bias from the crowd entering the pipeline.
* Once training data is created, employ toolkits for detecting and removing bias from machine learning models (either yourself, your developer or if you are thinking of outsourcing your AI to external companies/partners)
* Consider your partnerships and collaborators closely, including the ramifications of outsourcing your AI to external companies/partners to a 
* Know your data by creating a Factsheet describing and documenting it in full. (Example for AI models)


Resource(s):


Coleman, C. N. (2020). Managing Bias When Library Collections Become Data. International Journal of Librarianship, 5(1), 8–19. https://doi.org/10.23974/ijol.2020.vol5.1.162 

Eun Seo Jo and Timnit Gebru. 2020. Lessons from archives: strategies for collecting sociocultural data in machine learning. In Proceedings of the 2020 Conference on Fairness, Accountability, and Transparency (FAT* '20). Association for Computing Machinery, New York, NY, USA, 306–316. DOI:https://doi.org/10.1145/3351095.3372829
