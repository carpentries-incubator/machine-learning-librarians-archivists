---
title: "Introduction to AI and Machine Learning for GLAM"
teaching: 10
exercises: 5
questions:
- "What are Artificial Intelligence (AI) and Machine Learning (ML)?"
objectives:
- "Understand Machine Learning as a subfield of AI and name two others"
- "Name four types and machine learning and describe the difference between supervised and unsupervised learning"
- "Describe the difference between a model of data, and a model trained on data"


keypoints:
- "Machine Learning is a subfield of AI which identifies patterns in data"
- "Supervised learning algorithms learn by example"
- "Unsupervised learning algorithms put data into groups of similar objects or records"
---

## Artifical Intelligence and Machine Learning

The field of Artificial Intelligence has been around since the 1950s (ref: Dartmouth Conference). It is a broad topic which encompasses a number of sub-fields including but not limited to: Logic, Probability, Knowledge Representation, and Machine Learning.

This figure shows how a system based on Artificial Intelligence might function:


![AI process](../fig/ep-02-ai-graph.png)

The system accepts an input, performs some inference about what the input represents, performs some reasoning about the inferences made based on prior knowledge, and finally decides on an action.

### From logic to learning
The history of Logic stretches all the way back to The Organon of Aristotle (date?) and was formalised as a mathematical discipline by George Boole in the 19th century (hence the name Boolean Logic). With logic we can write rules to reason about data or make decisions.
 - “**It is** raining therefore I will carry an umbrella”.

Logical rules are based on things being True or False but the world is not so clear cut. Probability lets us add doubt and uncertainty:
- “It **might** rain today, should I take an umbrella?”.

With logical rules and probability we can solve quite complex tasks, but there are limits:
- “Which paintings in our collection have umbrellas in them?”.

Take a minute to think of how you would describe an umbrella using a set of rules:
- What colour is it?
- What shape is it?
- How big is it?
- What difference does it make if it is up or down?
- Is a parasol an umbrella?

Describing something as intuitively simple as an umbrella is difficult because although we have a rough conceptual idea there isn't a fixed physical description. Even if you break it into component parts you still need to define them - what is a handle? what is a canopy?
It becomes even more complicated if you try to specify the description in a way that a computer can interpret.
Thankfully Machine Learning can come to our rescue.

## What is Machine learning?

Machine Learning is a set of technologies and methods for finding rules when they are too complex to define. There are four types of machine learning:
- Supervised - learning by example
- Unsupervised - puts data into groups without guidance
- Semi-supervised - a combination of supervised and unsupervised
- Reinforcement - learns about the world by interacting with its environment

The fourth category has grabbed a lot of media attention as it is the basis for AlphaGo [ref] and driverless cars. This lesson will concentrate on Supervised and Unsupervised learning.


## Activity

Which of the following do you think would use Machine Learning?

- Counting the number of people in a museum using information from entry and exit barriers?
- A search system that looks for images similar to a user submitted sketch.
- A system that recommends library books based on what other users have ordered.
- A queueing system that spreads people evenly between 5 ticket booths
- A program which extracts names from documents by finding all capitalised words and checking them against a list of known names
- A system which turns digitised handwritten documents into searchable text
- A robot which cleans the vases in a museum without bumping into them or breaking them

  ## Solution
  - The sketch based search, book recommendation system, handwriting recognition, and robot cleaner, are all examples where machine learning would be needed. The others could all be achieved via rules.

  {: .solution}
{: .challenge}

## The two tasks of machine learning

There are two primary tasks in Machine Learning: prediction and classification.

Prediction is generally reserved for numerical data: how much will temperature control in the archive cost if we have a hot summer? how many days will library borrowers keep books for?
Classification is about categorising or labelling data: which paintings are of animals/architecture/people? which documents should be classified as sensitive?

Imagine you want to go on holiday next month. Imagine! You would like to know what the temperature will be on a small island that has no weather information. To do this you find the following information about other countries around the world: latitude, longitude, month, average temperature. Now you can use a machine learning technique called Regression to predict the temperature at your potential destination using its lat/lon and the month. This is a prediction task.

An alternative approach would be to make a list of destinations you like, and those you don’t like. Gather the same information of lat/lon, month and temperature for a sample of countries, but this time add a 'Yes' or 'No' for whether you like them or not. You can now choose one of many machine learning classification algorithms to label the rest of the world’s countries Yes or No. This is a binary (there are two categories) classification task.


## Supervised vs unsupervised learning

The previous example was of supervised learning. In the supervised scenario a set of labelled examples are passed to a machine learning classifier which learns to identify relationships between features of the data and the labels, or a numerical output. The table shows some examples of features and labels for some supervised learning tasks:

|Task|Application|Features|Output|Example learned relationship|
|----|----|----|----|----|
|Classification|Sentiment analysis|Words in a sentence|'Positive' or 'Negative'|'glad' or 'happy' weighted towards 'Positive' label|
|Classification|Seasonal paintings|Images of paintings|'Spring','Summer','Autumn','Winter'|Red leaves more predictive of Autumn label|
|Prediction|Child height estimate|Age of child|number in centimetres|Height increases as age increases|

Unsupervised learning is not given any examples. Instead a target is suggested and the algorithm groups the data based on that target. The target is usually the number of groups wanted, and the algorithm will place data points into each group in order to maximum the similarity of group members. The following activity aims to give you an intuition for clustering, a commonly used form of unsupervised learning.

## Activity

Imagine there are 6 people in a workshop and you need to split them evenly between 2 tables based on the similarity of their interests. Their interests are listed below in order of preference. How would you divide them into 2 tables with 3 people on each table?
- Person A - politics, sport, nature
- Person B - walking, cooking, quiz shows
- Person C - baking, sewing, athletics
- Person D - newspapers, biographies, history
- Person E - football, rugby, cricket
- Person F - fine dining, pub quizzes, bird watching

  ## Solution
  There isn't a right answer to this challenge. In fact an algorithm with no other information other than the words above would probably distribute them randomly. To perform the task it would need further information that could provide semantic relationships between the words. That may it could establish that sport is similar to football, rugby and cricket, and fine dining and cooking are related. Without that information they are just meaningless strings to a computer. You should have seen that there are multiple solutions and when using unsupervised methods you have little influence over which is chosen.

  {: .solution}
{: .challenge}

Each paradigm has its advantages and disadvantages. Unsupervised learning is a straightforward way of identifying clusters of similar records in a set of data making it ideal for gaining a high level view of a new dataset. However, choosing the right number of clusters can be difficult and there is no way to control the criteria for how clusters are formed. In the above exercise we saw a number of types of activity (physical, food related, current affairs, natural world), with some possibly fitting into two categories.
In supervised learning we define the categories in advance giving us control over the outputs. The downside is the cost of labelling our data. Consider the effort involved in the following tasks:

- Transcribing 100 pages of handwritten medieval documents
- Tagging each of 10000 images if they contain an umbrella
- Linking together daily visitor data with weather data currently held on someone else's website

## Activity

Fill in the blanks with either "Supervised Learning", "Unsupervised Learning", "Prediction" or "Classification"

- Estimating how much money a customer will spend in the museum shop is a _____ task
- A program to decide if a customer is a 'big spender' or a 'browser' would use a _____ algorithm
- Identifying four types of library visitor is an example of _____
- _____ requires labelled examples

  ## Solution
  - Estimating how much money a customer will spend in the museum shop is a Prediction task
  - A program to decide if a customer is a 'big spender' or a 'browser' would use a Classification algorithm
  - Identifying four types of library visitor is an example of Unsupervised Learning
  - Supervised Learning requires labelled examples

  {: .solution}
{: .challenge}

## Models and Algorithms

There is a lot of jargon and terminology in Machine Learning, and it can be confusing to a newcomer especially when some terms have more than one meaning. The term **model** is one such example.  In this episode we will present two definitions of model, and also introduce the term **algorithm**.

### Modelling the world

Whether the task is prediction or classification, the method supervised or unsupervised, the underlying principle is one of modelling the world through data.

We as humans are making models all the time. A quick look out the window and our in-built weather model, learned from past soakings, helps us make the umbrella decision. At school we learned some of the simplest models for numerical data - the average, the maximum and the minimum.
If I were to guess the height of the next person to walk through the door, the average would be a good model to use. If I were building the door then that would not be a good model as everyone above average height would have to stoop to enter (unless perhaps I were a Medieval Monarch…), so the maximum height might be a better starting point.
If average is the **conceptual model** I've chosen then I need some data, say, the height of all 19 year olds in Finland. To apply this model to the data I need an algorithm. We will use a simple **algorithm** that you probably learned as a child: add up all the heights and then divide by the number of measurements.
The value returned is 173.5cm (according to Wikipedia). That value is now my **trained model**.
If you give me the name of any 19 year old Finnish person my model will tell you their height - 173.5cm.

It will be wrong a lot of the time but there is a famous aphorism in the statistical and machine learning communities:

  "All models are wrong, some are useful" - George Box (1976)

In machine learning we have lots of models to choose from, and choosing a model depends on the type of data, the amount of data, the purpose, and a certain amount of pragmatism.

Before getting to GLAM specific scenarios and data, we will look at simple data to develop some intuition around modelling concepts. The following diagram shows four plots of data points with various linear models fit to the data. The data points were generated by some unknown process (unknown to the reader at least. It is a mathematical function that takes a number in and returns another number). The task of machine learning is to estimate what that function might be using example data generated by it (if we knew what the function was we wouldn't need ML). To make the task harder for the algorithm, random noise (errors) has been added to the data to mask the true process. This replicates what we experience in the real world, there's always something we can't capture in our models, or some error in our measurements. Typical examples we may encounter in cultural heritage are errors in transcription, or poorly digitised images.

![4 modelling plots](../fig/ep-02-4-plots.png)

The image contains 4 plots. The horizontal axis represents the input values and the vertical axis the outputs. Notice there are no labels on the axes. What the axes represent is not important to the algorithm, it is only mapping an input value to an output - two numbers.

Plot A shows three example data points (the crosses) and a straight line running between them. With this bare minimum amount of training data we have used the simplest possible **conceptual model** - there is a straight line relationship between input and output. We then chose an algorithm called Least Squares (invented by Carl Frederick Gauss in around 1795) to find the best line for this data. By best we mean that it found a model that makes predictions using the training data inputs that are as close as possible to the training data output. The **trained model** is the red line - or rather it is a formula that could be used to draw the red line. We can now use that formula to make predictions. Although this model is **wrong** (the real relationship is not a straight line), it may still be **useful** and satisfy our requirements. When the model is simpler than the true function, we call it **underfitting**.

In plot B there are 40 training data points. With more data we can try out more complex models. The red dotted line represents a very complex model which is able to draw quite intricate curves. The grey dashed line is a simpler model (it is only allowed to bend twice) and is actually the closest approximation to the underlying process that generated the data. What we can see here is that the red line is too wiggly, it is following the data points more closely because it been given the freedom to do so. This is an example of a phenomenon known as **overfitting**. The model has fit itself to the training data but it has learned the wrong pattern and would not generalise well to data it has not seen before - it is learning as much about the added noise as the true function.
In machine learning we always work with two sets of data. The training data is used to train the model, the testing data is used to verify whether the model will generalise to unseen data. It is important that the training data and testing data are both representative of the real world data we will use our model against in an application but they must not overlap with each other.
The process of training a model is often called the Data Science Lifecycle. It is an iterative process of finding the best model using training data. The very end of this process is when the test data is used, and often in competitive situations (e.g. an academic competition, or private companies competing for a tender) the test data is not seen by the data scientists at all.

Plot C shows the simple model (red dotted line) from Plot B but this time it is trained on only 10 data points. The dashed grey line is the true function and we can see that our model matches it pretty closely. Contrast this with Plot B where the complex model struggled to work out the true curve with 40 data points.

Plot D again shows the same models as Plot B but this time they are trained on 500 data points. Now both curves look the same. With more data available the complex model has now been able to see through the noise and find the true pattern in the data.

The point of plots C & D, and to some extent A, is that we should try to choose the simplest model for our purposes. A complex model can learn any pattern given enough data, but often the simpler one is enough or even better and needs less data (which we know is resource intensive to create).

### Modelling summary
- With small amounts of data available we need to simplify our model of the world
- An overly complex model can fit too closely to training data, a process called **overfitting**
- The opposite of overfitting is **underfitting**. This means the model is too simple, as in the case of the straight line model.
- A simple model may still be good enough for our purposes
- If we want to model the complexities of the world, we need more data



## GLAM data and Machine learning

In a GLAM setting we rarely work with numerical data and are far more likely to be working with images and text. For these we need to turn to the fields of Computer Vision and Natural Language Processing, respectively.

### Computer Vision

Computer Vision (often abbreviated to CV) has been around since the early days of AI but has been revolutionised in recent years by so called Deep Learning models. The most common of these models is called a Convolutional Neural Network (CNN) and is capable of identifying complex patterns in images. A **convolution** is inspired by our own visual system. Imagine you are travelling at high speed and trying to avoid obstacles. Your visual system doesn't have time to work out the fine details of the objects in front of you, it just needs to detect shapes. Convolutions work in that way too. One convolution may detect horizontal edges, another vertical edges, yet another corners, and so on. They work over very small portions of an image, as little as 3x3 pixel squares. A **neural network** is a complex machine learning model which we use when we need to go beyond drawing lines between points (although they can do that too). It is built of layers of numbers and data is passed through the layers until an answer of some sort comes out of the other end. In a CNN the first layer find the edges, the second layer starts to find patterns of connected edges, the third layer may start to detect shapes, and we keep going until the final layer when a classification is decided on based on all the patterns found in the image. A Deep Convolutional Neural Network (quite a mouthful) is just the name for a CNN with lots of layers (there can be hundreds). The deeper the network, the more complex features it can identify in an image - from edges, to shapes, to patterns, to textures. However, as we learned in the linear model section, complexity comes at a cost. A deep network may need to see millions of labelled images to perform well, and they can take many hours, days, or even weeks to train.

You can play with a small neural network and see convolutions in action at [Tensorflow Playground](https://playground.tensorflow.org/)
You don't need to know anything about neural networks, just try things out and see what happens - sometimes even the professionals do that!

The challenge with modelling images is that they are complicated but we have methods for simplifying them. If we simplify the images then we may be able to simplify our model and therefore use a smaller training set. Again it all comes down to our purpose and what is good enough to achieve that to a satisfactory level.
A colour image is made up of pixels, the tiny dots that combine to make the picture. A typical image taken by your phone camera may be in the region of 3000 pixels high by 2000 pixels wide. That is 6,000,000 pixels in total. Each pixel is represented by 3 numbers between 0 and 255 which are the amounts of Red, Green and Blue in the pixel. This means there are over 16 million possible colour values. This is a lot for even advanced machine learning algorithms to take in but luckily it is also unnecessary for most tasks. If you think about browsing images on your phone you generally see thumbnail images. We don't see all the detail of the image but there is enough to get a good idea of what each photo is. So often the first step in image classification is to shrink the images to a standard size, say, 28x28 pixels. This sounds tiny but it is enough for a trained algorithm to tell the difference between a cat and a dog, or a motorbike and a car. It's enough for our eyes afterall. By doing this we've reduced the problem from 6,000,000 data points per image to 784.
The other thing we can do is to simplify the colours. One option is to convert to grayscale which converts the 3 numbers to a single value between 0 and 255. This represents 254 shades of grey in-between 0 (black) and 255 (white). Again this is a massive reduction in complexity from over 16 million potential values in each pixel to only 255. We can go further still and make our images binary - 0 for dark colours, 1 for light.

#### Computer Vision tasks

- Object detection: identify buildings, people, vehicles or animals in images
- Object classification: label images according to a set of categories


#### Thinking about object detection

At the beginning of the episode we thought about how we might build a set of rules to describe an umbrella. Now we know that with machine learning we can provide an algorithm with images containing umbrellas, and images without umbrellas.

Take a look at pictures labelled as umbrellas in the image collections of the Smithsonian Institute, British Library, and The National Archives (UK).
- [Smithsonian Images](https://www.si.edu/search/collection-images?edan_q=umbrella&edan_fq%5B0%5D=unit_code%3AAECI%20OR%20unit_code%3ASAAM%20OR%20unit_code%3ASAAMPAIK%20OR%20unit_code%3ASAAMPHOTO%20OR%20unit_code%3ASAAM_BL%20OR%20unit_code%3ASAAM_PC%20OR%20unit_code%3ASAAM_YT%20OR%20unit_code%3AARI%20OR%20unit_code%3ACHNDM%20OR%20unit_code%3ACHNDM_BL%20OR%20unit_code%3ACHNDM_YT%20OR%20unit_code%3ANPG%20OR%20unit_code%3ANPGCAP%20OR%20unit_code%3ANPG_BL%20OR%20unit_code%3ANPG_PC%20OR%20unit_code%3ANPG_YT&edan_fq%5B1%5D=media_usage%3A%22CC0%22)
- [British Library](https://www.flickr.com/search/?user_id=12403504%40N02&view_all=1&text=umbrella)
- [National Archives](https://images.nationalarchives.gov.uk/assetbank-nationalarchives/action/quickSearch?CSRF=tjiJXkCDwWWQyYGpBvAF&newSearch=true&quickSearch=true&includeImplicitCategoryMembers=true&keywords=umbrella)

Now think back to some of the questions we asked earlier:
- Is colour important?
- What compromises do you think you'd have to make if you could only label small amounts of training data?
- The umbrella classifier needs counter examples - pictures without umbrellas - what kind of images would you use for those? [Hint: think of things which might be mistaken for umbrellas]

{: .discussion}

### Natural Language Processing

In Computer Vision we started with a grid of numbers which is the way that images are represented in a computer. Machine Learning algorithms need numerical inputs which means that before we can work with text we need to convert it into a numerical form.
This means there are two stages to modelling our data, each introducing assumptions about the world which impact the tasks we can accomplish, and the computational and data resource needed to accomplish them.

Stage one is to model the words in our text. The simplest way is to build a vocabulary and then count how many times each word in the vocabulary appears in each document. The vocabulary is generally built from the training corpus because the classifier needs at least one example of each word. In recent years state of the art systems have used a representation of words called **word embeddings**. Conceptually embeddings are numerical representations of words which allow us to find semantically similar words. This means that if our training corpus contains the words 'tree', 'plant' and 'flower', then applying the model to a document containing the word 'bush' will still work even though it wasn't in the training corpus.
Word embeddings are often trained on a very large corpus of documents (e.g. Wikipedia) and made publicly available. While this is convenient it is important to bear in mind that the documents they're trained on may not be representative of the language encountered in historical documents.

The second stage is to model the language. This doesn't mean creating a complex linguistic model, but thinking about simplifying assumptions about the text to reduce computational complexity. The simplest language model considers all words in a sentence to be independent of each other.
- Do you think that is a reasonable assumption?

If you were formulating a theory of language it would be a bad assumption, as it suggests sentences are random sets of words. However, for many real world machine learning tasks it works quite well. The term **bag of words** is often used to describe such a model. One way of thinking of this model of language is to imagine writing a review of a book. In front of you are two bags, one marked 'Positive' and the other 'Negative'. If you like the book you will reach into the 'Positive' bag for words to use in your review, and if you don't like it then you choose words from the 'Negative' bag.
Now a Machine Learning algorithm trying to learn a model for identifying whether reviews are positive or negative is effectively trying to establish which bag the words in the review came from.
The reviews containing words like 'Interesting', 'Exciting', 'Delightful' are more likely to be positive, while 'Boring' and 'Uninteresting' would suggest the negative bag was used.
The simplicity of the model allows us to use less training data and would be computationally efficient to build a model.

Of course we know that language is more nuanced than that.
- "The book was not boring at all" - this sentence is positive despite the word 'boring' appearing in it.
- "The author's other books were exciting but this was not" - this sentence is negative despite containing 'exciting'

In this case we can increase the complexity of our language model to use pairs of words, which would mean 'not boring' becomes a feature in the input data. However, remember that whenever we increase complexity we generally need more data.

Modern deep learning models are able to model sentences, or even paragraphs and documents, as strings of related words. This is essential for tasks such as machine translation where word order changes between languages. It is also necessary if we want the machine to make sense of long passages where perhaps the subject of the sentence was mentioned at the beginning but is referred to by a pronoun later on in the document.

- Otto met Nancy at the park. It was a beautiful sunny day and he was looking forward to their picnic together.

The kind of machine learning model needed to make the connection between 'their' and 'Otto and Nancy' is called a **Recurrent Neural Network (RNN)**. Recurrent just means that it models its inputs as a sequence and is able to make connections between items in the sequence.
As always, there is a trade off. Complex deep learning models require a lot of training data, millions of lines of text to perform well. This makes sense because to identify relationships between words it must see examples of words used in different contexts.

## Activity

Which of these typical Natural Language Processing tasks do you think requires a complex language model, and which could be achieved with a simpler one.

- Sentiment analysis: Is a sentence positive or negative?
- Machine Translation: converting text in one language, to another
- Spam detection
- Entity extraction: identifying people, places, organisations in text
- Text generation: generating text, maybe a poem, in the style of an author
- Question answering: interpreting a written question and retrieving the answer from a database

  ## Solution
  - Sentiment analysis: this can work with bag of words but things like sarcasm are difficult to detect.
  - Machine Translation: definitely requires a complex model due to changes in word order, idiomatic phrases that don't translate well, and translations not being a one to one mapping of words.
  - Spam detection: simple models work remarkably well as spam is often full of obvious keywords
  - Entity extraction: named entities often fit standard patterns so a simple model works quite well
  - Text generation: generating plausible looking text requires a huge amount of training data but not necessarily a complex model. Generating text that makes sense is a much more complex problem.
  - Question answering: this can be achieved with a simple model. It is as much about identifying patterns of questions, and depends on how controlled the domain of questions is. For example, answering "What time is the next train to London?" does not require a complex language model.
  {: .solution}
{: .challenge}

### Computer Vision meets Natural Language Processing

One of the state of the art applications of machine learning seen in cultural heritage at the moment is Handwritten Text Recognition (HTR). The idea is to convert digitised handwritten documents into searchable and machine readable text.
To achieve this HTR uses a combination of Computer Vision and Natural Language Processing. A Convolutional Neural Network is used to work out the letter shapes in each word. Since handwriting can be tricky and ambiguous the best it can do is identify possible letters from the shapes it has identified. A Recurrent Neural Network is then used to work out the most likely word. Since it has a sentence level language model it does this by taking into account words in the whole line of text so that it can use context to work out the most likely word. By balancing the prediction of the Computer Vision model with the language model it is still able to output words that were never seen in the training data.
