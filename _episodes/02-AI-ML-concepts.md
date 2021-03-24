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

## What is the difference between Machine Learning and AI?

The field of Artificial Intelligence has been around since the 1950s (ref: Dartmouth Conference). It is a broad topic which encompasses a number of sub-fields including but not limited to: Logic, Probability, Knowledge Representation, and Machine Learning.

Figure 1 shows how a system based on Artificial Intelligence might function:


![AI process](ai_graph.png)


### From logic to learning
The history of Logic stretches all the way back to The Organon of Aristotle (date?) and was formalised as a mathematical discipline by George Boole in the 19th century (hence the name Boolean Logic). With logic we can write rules to reason about data or make decisions.
 - “**It is** raining therefore I will carry an umbrella”.

Logical rules are based on things being True or False but the world is not so clear cut. Probability lets us add doubt and uncertainty:
- “It **might** rain today, should I take an umbrella?”.

With logical rules and probability we can solve quite complex tasks, but there are limits:
- “Which paintings in our collection have umbrellas in them?”.

{: .challenge}
Take a minute to think of how you would describe an umbrella using a set of rules:
- What colour is it?
- What shape is it?
- How big is it?
- What difference does it make if it is up or down?
- Is a parasol an umbrella?

## Machine learning

Machine Learning is a set of technologies and methods for finding rules when they are too complex to define. There are four types of machine learning:
- Supervised - learning by example
- Unsupervised - puts data into groups without guidance
- Semi-supervised - a combination of supervised and unsupervised
- Reinforcement - learns about the world by interacting with its environment

The fourth category has grabbed a lot of media attention as it is the basis for AlphaGo [ref] and driverless cars. This lesson will concentrate on Supervised and Unsupervised learning.


{: .challenge}
Which of the following do you think would use Machine Learning?

- Counting the number of people in a museum using information from entry and exit barriers?
- A search system that looks for images similar to a user submitted sketch.
- A system that recommends library books based on what other users have ordered.
- A queueing system that spreads people evenly between 5 ticket booths
- A program which extracts names from documents by finding all capitalised words and checking them against a list of known names
- A system which turns digitised handwritten documents into searchable text
- A robot which cleans the vases in a museum without bumping into them or breaking them


## The two tasks of machine learning

There are two primary tasks in Machine Learning: prediction and classification.

Prediction is generally reserved for numerical data: how much will temperature control in the archive cost if we have a hot summer? how many days will library borrowers keep books for?
Classification is about categorising or labelling data: which paintings are of animals/architecture/people? which documents should be classified as sensitive?

Imagine you want to go on holiday next month. Imagine! You would like to know what the temperature will be on a small island that has no weather information. To do this you find the following information about other countries around the world: latitude, longitude, month, average temperature. Now you can use a machine learning technique called Regression to predict the temperature at your potential destination using its lat/lon and the month. This is a prediction task.

An alternative approach would be to make a list of destinations you like, and those you don’t like. Gather the same information of lat/lon, month and temperature for a sample of countries, but this time add a 'Yes' or 'No' for whether you like them or not. You can now choose one of many machine learning classification algorithms to label the rest of the world’s countries Yes or No. This is a binary (there are two categories) classification task.


## Supervised vs unsupervised learning

The previous example was of supervised learning. In the supervised scenario a set of labelled examples are passed to a machine learning classifier which learns to identify relationships between features of the data and the labels, or a numerical output.
- Words such as 'glad', 'happy' or 'pleased' more indicative of 'Positive' label
- Light blue colours in a painting help predict 'Summer' label
- An increase in a child's age leads to an increase in height

Unsupervised learning is not given any examples. Instead a target is suggested and the algorithm groups the data based on that target. The target is usually the number of groups wanted, and the algorithm will place data points into each group in order to maximum the similarity of group members.

{: .challenge}
Imagine there are 6 people in a workshop and you need to split them evenly between 2 tables based on the similarity of their interests. Their interests are listed below in order of preference. How would you divide them into 2 tables?
- Person A - politics, sport, nature
- Person B - walking, cooking, quiz shows
- Person C - baking, sewing, athletics
- Person D - newspapers, biographies, history
- Person E - football, rugby, cricket
- Person F - fine dining, pub quizzes, bird watching

Each paradigm has its advantages and disadvantages. Unsupervised learning is a straightforward way of identifying clusters of similar records in a set of data making it ideal for gaining a high level view of a new dataset. However, choosing the right number of clusters can be difficult and there is no way to control the criteria for how clusters are formed. In the above exercise we saw a number of types of activity (physical, food related, current affairs, natural world), with some possibly fitting into two categories.
In supervised learning we define the categories in advance giving us control over the outputs. The downside is the cost of labelling our data. Consider the effort involved in the following tasks:
- Transcribing 100 pages of handwritten medieval documents
- Tagging each of 10000 images if they contain an umbrella
- Linking together daily visitor data with weather data currently held on someone else's website

{: .challenge}
Fill in the blanks with either "Supervised Learning", "Unsupervised Learning", "Prediction" or "Classification"

- Estimating how much money a customer will spend in the museum shop is a _____ task
- A program to decide if a customer is a 'big spender' or a 'browser' would use a _____ algorithm
- Identifying four types of library visitor is an example of _____
- _____ requires labelled examples

## Modelling the world

Whether the task is prediction or classification, the method supervised or unsupervised, the underlying principle is one of modelling the world through data.

We as humans are making models all the time. A quick look out the window and our inbuilt weather model, learned from past soakings, helps make the umbrella decision. At school we learned some of the simplest models for numerical data - the average, the maximum and the minimum.
If I were to guess the height of the next person to walk through the door, the average would be a good model to use. If I were building the door then that would not be a good model as everyone above average height would have to stoop to enter (unless perhaps I were a Medieval Monarch…), so the maximum height might be a better starting point.
In machine learning we have lots of models to choose from. Categories of model include:
- Linear: find a line that roughly follows the pattern of the data
- Boundary: separates different categories of data by placing a boundary between them
- Sequential: the data is in a sequence and the model can take into account what has come before, and what is yet to come.

Which of the above three models do you think would be most appropriate for modelling text documents?

Choosing a model depends on the type of data, the amount of data, the purpose, and some pragmatism.

Before getting to GLAM specific scenarios and data, we will look at simple linear data to develop some intuition around modelling concepts. The following diagram shows four plots of data points with various linear models fit to the data. The data points were generated by some unknown process (a mathematical function that takes a number in and returns another number). The task of machine learning is to estimate what that function might be using example data generated by it. To make life harder for the ML random noise (errors) has been added to the data to mask the true process. This replicates what we experience in the real world, there's always something we can't capture in our models.

![4 modelling plots](4_plots.png)

Plot A shows the simplest model we can build. The model assumes a straight line relationship between the input and output numbers, as the input increases, the output increases by a predictable amount. Although this model is wrong (the real relationship is not a straight line), it may still be useful and satisfy our requirements.
Plot B shows two models together. This time the models are trained using 40 examples and a curved pattern emerges. The red dotted line represents a very complex model which is able to draw quite intricate curves. The grey dashed line is a simpler model and is actually the closest approximation to the underlying process that generated the data. What we can see here is that the red line is too wiggly, it is following the data points more closely because it is allowed to. This is an example of a phenomenon known as **overfitting**. The model has fit itself to the training data but it would not work well with new data - it is learning as much about the added noise as the true function.
Plot C shows the simple model (red dotted line) from Plot B but this time it is trained on only 10 data points. The dashed grey line is the true function and we can see that our model matches it pretty closely. Contrast this with Plot B where the complex model struggled to work out the true curve with 40 data points.
Plot D again shows the same models as Plot B but this time they are trained on 500 data points. Now both curves look the same. With more data available the complex model has now been able to see through the noise and find the true pattern in the data.

### Modelling summary
- With small amounts of data available we need to simplify our model of the world
- An overly complex model can fit too closely to training data, a process called **overfitting**
- The opposite of overfitting is **underfitting**. This means the model is too simple, as in the case of the straight line model.
- A simple model may still be good enough for our purpose
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


#### {: .challenge} Thinking about object detection

At the beginning of the episode we thought about how we might build a set of rules to describe an umbrella. Now we know that with machine learning we can provide an algorithm with images containing umbrellas, and images without umbrellas.

Take a look at pictures labelled as umbrellas in the image collections of the Smithsonian Institute, British Library, and The National Archives (UK).
- [Smithsonian Images](https://www.si.edu/search/collection-images?edan_q=umbrella&edan_fq%5B0%5D=unit_code%3AAECI%20OR%20unit_code%3ASAAM%20OR%20unit_code%3ASAAMPAIK%20OR%20unit_code%3ASAAMPHOTO%20OR%20unit_code%3ASAAM_BL%20OR%20unit_code%3ASAAM_PC%20OR%20unit_code%3ASAAM_YT%20OR%20unit_code%3AARI%20OR%20unit_code%3ACHNDM%20OR%20unit_code%3ACHNDM_BL%20OR%20unit_code%3ACHNDM_YT%20OR%20unit_code%3ANPG%20OR%20unit_code%3ANPGCAP%20OR%20unit_code%3ANPG_BL%20OR%20unit_code%3ANPG_PC%20OR%20unit_code%3ANPG_YT&edan_fq%5B1%5D=media_usage%3A%22CC0%22)
- [British Library](https://www.flickr.com/search/?user_id=12403504%40N02&view_all=1&text=umbrella)
- [National Archives](https://images.nationalarchives.gov.uk/assetbank-nationalarchives/action/quickSearch?CSRF=tjiJXkCDwWWQyYGpBvAF&newSearch=true&quickSearch=true&includeImplicitCategoryMembers=true&keywords=umbrella)

Now think back to some of the questions we asked earlier:
- Is colour important?
- What compromises do you think you'd have to make if you could only label small amounts of training data?
- The umbrella classifier needs counter examples - pictures without umbrellas - what kind of images would you use for those? [Hint: think of things which might be mistaken for umbrellas]


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
- "The book was not boring at all"
- "The author's other books were exciting but this was not"

Modern deep learning models are able to model sentences, or even paragraphs and documents, as strings of related words. This is essential for tasks such as machine translation where word order changes between languages. It is also necessary if we want the machine to make sense of long passages where perhaps the subject of the sentence was mentioned at the beginning but is referred to by a pronoun later on in the document.

- Otto met Nancy at the park. It was a beautiful sunny day and he was looking forward to their picnic together.

The kind of machine learning model needed to make the connection between 'their' and 'Otto and Nancy' is called a **Recurrent Neural Network (RNN)**. Recurrent just means that it models its inputs as a sequence and is able to make connections between items in the sequence.
As always, there is a trade off. Complex deep learning models require a lot of training data, millions of lines of text to perform well. This makes sense because to identify relationships between words it must see examples of words used in different contexts.

Typical tasks in Natural Language Processing include:
- Sentiment analysis: Is a sentence positive or negative?
- Machine Translation: converting text in one language, to another
- Spam detection
- Entity extraction: identifying people, places, organisations in text
- Text generation: generating text, maybe a poem, in the style of an author
- Question answering: interpreting a written question and retrieving the answer from a database

{: .challenge} Which of these tasks do you think requires a complex language model, and which could be achieved with a simpler one.

### Computer Vision meets Natural Language Processing

One of the state of the art applications of machine learning seen in cultural heritage at the moment is Handwritten Text Recognition (HTR). The idea is to convert digitised handwritten documents into searchable and machine readable text.
To achieve this HTR uses a combination of Computer Vision and Natural Language Processing. A Convolutional Neural Network is used to work out the letter shapes in each word. Since handwriting can be tricky and ambiguous the best it can do is identify possible letters from the shapes it has identified. A Recurrent Neural Network is then used to work out the most likely word. Since it has a sentence level language model it does this by taking into account words in the whole line of text so that it can use context to work out the most likely word. By balancing the prediction of the Computer Vision model with the language model it is still able to output words that were never seen in the training data.

## Episode summary

In this episode we have learned:

- How machine learning is a part of the field of Artificial Intelligence
- The difference between Supervised and Unsupervised learning
- That machine learning starts with a model of the data
- Modelling is about compromising according to purpose, amount of data and available computing power.
