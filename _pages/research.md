---
title: "Research"
layout: default
excerpt: "RT2 Lab -- Research"
sitemap: false
permalink: /research/
---

# Research

## Human–computer interaction

### Vietnamese Automatic Speech Recognition

<p align="center">
  <img src="{{ site.url }}{{ site.baseurl }}/images/research/asrsystem.png" width="100%" 
  title="ASR System">
</p>
<p align="center">Automatic Speech Recognition System</p>

ASR Systems try to map each signal input to the corresponding text. The architecture of ASR Systems typically includes Feature Extractor, Acoustic Model (Encoder) and Decoder. In many situations, Language Model might be used to improve prediction accuracy. After being extracted by Feature Extractor, data are encoded by the Encoder and decoded by the Decoder to produce the text. Click <a href="https://asr-bilhfc3vqa-as.a.run.app/">here</a> for ASR demonstration.

### Chatbot for restaurant booking service

Currently, the demand for direct interaction between businesses and customers is increasing. Science and technology is constantly evolving, Chatbot has been launched to solve the above needs for companies and businesses. Chatbots are used in many topics depending on the scenario built for bots. In the topic of restaurant booking service, the chatbot was created to interact with customers in the most natural way but still solve the customer's needs and get the most accurate information of the customer.

There are many frameworks for creating chatbots, one of which is the Rasa framework. The framework acts as the expected conversational flow which makes it feel more like a human interaction. This framework consists of two parts: Rasa NLU to determine user intent and Rasa Core based on user intent to decide a next action to be performed by the bot as the script is built.

<p align="center">
  <img src="{{ site.url }}{{ site.baseurl }}/images/research/rasa_architecture.png" width="100%" 
  title="ASR System">
</p>
<p align="center">Rasa NLU independent analysis system and independent action of Rasa Core <a href="https://rasa.com/blog/bending-the-ml-pipeline-in-rasa-3-0/">ref</a></p>

<p align="center">
  <img src="{{ site.url }}{{ site.baseurl }}/images/research/rasa_test_fanpage_facebook.png" width="100%" 
  title="ASR System">
</p>
<p align="center">Test chatbot Rasa in fanpage facebook</p>

### Emotion recognition
The problem of emotion recognition is a large area of research based on two subjects, which are emotional psychology and artificial intelligence. Human's emotions can be expressed through speech or nonverbal such as facial variations, tone of voice, etc and are recognized by sensor. In 1967, Mehrabian showed that 55% of emotions expressed from the face, 38% from the words voice and 7% from speech. That is why researchers are very interested in this field.  

Facial emotion recognition has many applications in variety of fields: 
- Education: learner's reactions to participating in the lesson.
- Examination: monitor and make predictions whenever contestants show signs of cheating.
- Marketing: how to receive information from buyers when listening about product offers.
- Security: helps detect suspicious behavior in the crowd and prevent threats potential opportunity.
- Medical: automate the care process and analyzing the mental health of users.
- Recruitment: evalutate candidate quality and interview process.

<p align="center">
    <img src = "{{site.url}} {{site.baseurl}}/images/research/fusion.png" width=80%
</p>
<p align="center">Combined Architecture</p>
### Electrocardiogram (ECG) classification

<p align="center">
  <img src="{{ site.url }}{{ site.baseurl }}/images/research/ecg_signal.png" width="80%" 
  title="ECG Signal">
</p>
<p align="center">ECG Signal</p>

Early detection and prediction of cardiac anomalies play an important role in the diagnosis and treatment of cardiovascular diseases. In medicine, electrocardiography provides valuable information for the doctors since they can accurately determine what is happening concerning the heart activities. Nevertheless, electrocardiography classification is a non-trivial challenge due to the specialties of these data as well as the reliability of manual data collection methods. This motivates IASLab's members to study electrocardiography signal classification method based on Deep Learning approach to handle data collected from intelligent IoT devices.

### Other related topics
- NLP/NLU
- Speech: text-to-speech (TTS)
- Biomedical signal processing: EEG, ECG, etc.


## AI for Healthcare

### Tumor Segmentation

<p align="center">
  <img src="{{ site.url }}{{ site.baseurl }}/images/research/lung_tumor_segmentation.png" width="90%" 
  title="Tumor Segmentation">
</p>
<p align="center">Lung Tumor Segmentation</p>

<p align="center">
  <img src="{{ site.url }}{{ site.baseurl }}/images/research/brain_tumor_segmentation.png" width="100%" 
  title="Brain Tumor Segmentation">
</p>
<p align="center">Brain Tumor Segmentation</p>

Nowadays, cancers is one of the most common causes of death. It is the growing of abnormal cells which is able to invade and destroy other cells and tissues; moreover, it can occur in any organ of the body. However, cancers can be treated if they're detected early. Therefore, some researches on this domain have been conducted by IASLab. We focus on detecting tumor of Lung and Brain.

Tumor Segmentation is the process of separating the tumor from a medical image (2D or 3D). It provides useful information for diagnosis, clinical studies and treatment planning. By using Deep Learining architectures, we got some promising results on both Lung and Brain tumor segmentation aims. This significantly encourages us to expand our jobs in Tumor Segmentation domain. 

<!-- - Lung cancer survival analysis
- etc. -->

## Others

We always extend our research topic to meet our life needed, if you found a topic is interested, feel free to raise.

### Computer Vision
- Pattern recognition
- Object detection
- etc.

### Time series analysis
- VNPT 4G telecom maintenance
- etc.

