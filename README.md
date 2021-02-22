# Simon_Says

## Inspiration

ASD is a neurodevelopmental disorder characterized by persistent deficits in social interaction and communication with restricted, repetitive patterns of behaviour, interests or activities.
The 2018 National Autism Spectrum Disorder Surveillance System (NASS) Report estimates autism's prevalence as 1 in 66 children in Canada. This includes 1 in 42 boys and 1 in 189 girls. An estimated 50,000 teens with autism become adults – and lose school-based autism services – each year.
For some people on the spectrum, life in lockdown is aggravating anxiety and other autism traits. Women and children with autism, and those living in group homes, seem particularly hard hit by the pandemic, although the experiences of autistic people have been almost as varied as the condition itself. During the coronavirus crisis, many families who have children with autism spectrum disorder are facing the suspension of both school and essential services that their children are used to receiving. Additionally, children with autism may have difficulty adjusting to changes in their routine and environment. Although different states and districts are handling these situations in a variety of ways and every family’s needs are unique, there are some common starting points for parents to consider as we all adjust to this “new normal.”
We were looking for a way to tackle this issue in favor of one of the biggest minorities around the world.


## What it does

Our website SimonSays is a daily task planner geared towards children with Autism Spectrum Disorder (ASD).  
Research has indicated that children performed better during interaction experiments with robotic artifacts with non-human facial appearance as they have difficulty with human interaction and avoid eye contact.
SimonSays integrates machine learning with a chat-bot that senses emotions and responds accordingly. Besides that it monitor the daily tasks defined by ASD kids' parents/mentors and help the ASD users to reach their goals. These activates could be be set up with the parent account.


## How we built it

Besides the features of this web app we needed to implement an intelligent chat bot which could recognize the Autism kids anxiety and depression and give them some tips to help them. Cognitive behavioral therapy (CBT) is a type of psychotherapy in which negative patterns of thought about the self and the world are challenged in order to alter unwanted behavior patterns or treat mood disorders such as depression. Using transcripts of therapy sessions, we can build the virtual human so that it can provide effective counselling not only for ASD kids but other adolescents. 
Also this chat bot was designed to remind the ASD kids regarding their daily task and tutor them with them.
Regarding the emotion detection we need to collect data we need to have a dataset to train our model. 1.6 million tweets from twitter, classified into positive (4) and negative (0), as the training data, of which 20% is used as cross validation data. 494 tweets from twitter, classified into positive (4), neutral (2) and negative (0), as the test data. Labels adjusted to be in the range 0 to 1.
Hashtags, website links and user references removed, then input tweets preprocessed by Gensim, with preprocessed tweets of length less than two removed. Vocabulary of words initialized with Gensim Dictionary and words replaced with respective position in the vocabulary plus one.
Preprocessed tweets of length less than 20 were zero-padded to length 20. Those of length greater than 20 were split into tweets of length 20 and the last split part zero-padded, if necessary. Zeropadding done for supplying variable length sequences to the LSTM layer.
After preparing the semantic analysis we deployed an NNA to train our model and did a cross validation to measure its accuracy and make sure our model is not over-trained. The results showed that our model has 83.32% accuracy.
We used our trained model in the chatbot. In this process our chatbot score the kid's answers with help of semantic analysis and give the user tips to help them with their tasks or calm them down when they are facing with a high level of anxiety which is a normal concern for the ASD kids.
Regarding the frontend we muted the palette colors since ASD children are hyper-sensitive to bright colors. We used the React to deployed our front end.
At the back end we used Google Cloud to host the web app, Firebase for login authentication, and database, Microsoft Azure Cognitive Services regarding the speech-to-text, text-to-speech with deep network for sound characters and IBM Watson for tone and sentiment analyzer.

# UI
<p>
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/349/043/datas/gallery.jpg" height="220"/>
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/349/047/datas/gallery.jpg" height="220"/>
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/349/296/datas/gallery.jpg" height="220"/>
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/349/049/datas/gallery.jpg" height="220"/>
</p>

## Challenges we ran into

In the first step, we needed to determine the priorities and difficulties of ASD kids. For that purpose since one of our members is a Sr. Head Staff in the "Variety - The Children's Charity of Ontario" we searched their databases for the recent studies.
Regarding training our model data collection and data labeling was one of the challenges we faced. In the first step we clustered our collected dataset with help of unsupervised techniques and classify them in four classes.
Since for most of ASD kids it is not easy to track the lines or type, there was a need of text-to-speech and speech-to-text API to handle the chatbot. We addressed that issue with help of Microsoft Azure Cognitive Services.

## Accomplishments that we're proud of

We are happy that we could create a hack that can decrease divisions and bring people with Autism disabilities together that improves the quality of  online learning for them and to improve some aspects of their public health.


## What's next for Simon Says

We have plan to make the website public and share our website with "Variety - The Children's Charity of Ontario" researchers to get experts feedbacks on it to improve our web app.

# Link
[Devpost](https://devpost.com/software/simon-says-zgr09i)
