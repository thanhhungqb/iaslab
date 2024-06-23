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

### Voice Cloning

Voice cloning is a task in text-to-speech (TTS) technology that allows for replicating a person's voice to speak a given text. Voice cloning can be applied in various fields, such as creating voice agents for banks and commerce. It can restore the voices of deceased individuals or those with speech impairments. Additionally, it can be used to generate voices for characters in video games, enhancing the gaming experience with more personalized and realistic character interactions.

<p align="center">
  <img src="../images/research/voice_cloning_overview.png" width="50%" 
  title="Image Captioning">
</p>
<p align="center">Voice Cloning System</p>

Although there are several ongoing studies in this field, challenges remain. The generated voice often lacks the naturalness of human speech, and it may not capture the unique characteristics of the reference voice accurately. These limitations highlight the need for further advancements to achieve more realistic and distinctive voice cloning results.

<p align="center">
  <img src="../images/research/voice_cloning_architecture.png" width="80%" 
  title="Image Captioning">
</p>
<p align="center">DGSpeech Architecture</p>

This project introduces DGSpeech, which is built on the FastSpeech2 architecture. DGSpeech incorporates:

- MixStyle Layer Normalization: this technique perturbs style information by mixing and shuffling style embeddings, enhancing robustness and generalization of TTS models to adapt to varying styles and domains.

- Flow-based Postnet: refines outputs from the transform decoder to produce more precise mel-spectrograms, enhancing the detail and quality of generated speech, particularly in expressive contexts.

Click [here](https://hungle45.github.io/tts-demo/) for Voice Cloning demonstration.

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
#### Image
The problem of emotion recognition is a large area of research based on two subjects, which are emotional psychology and artificial intelligence. Human's emotions can be expressed through speech or nonverbal such as facial variations, tone of voice, etc and are recognized by sensor. In 1967, Mehrabian showed that 55% of emotions expressed from the face, 38% from the words voice and 7% from speech. That is why researchers are very interested in this field.  

Facial emotion recognition has many applications in variety of fields: 
- Education: learner's reactions to participating in the lesson.
- Examination: monitor and make predictions whenever contestants show signs of cheating.
- Marketing: how to receive information from buyers when listening about product offers.
- Security: helps detect suspicious behavior in the crowd and prevent threats potential opportunity.
- Medical: automate the care process and analyzing the mental health of users.
- Recruitment: evalutate candidate quality and interview process.

<p align="center">
    <img src="{{ site.url }}{{ site.baseurl }}/images/research/late_fusion.png" width="80%" title="Combined Architecture" >
</p>

#### Video
Traditionally, facial emotion recognition has relied heavily on static images. However, in dynamic contexts such as videos, understanding temporal dynamics becomes crucial for accurate emotion interpretation. One approach to addressing this involves focusing on the most relevant frames within a video, rather than uniformly sampling frames. This is achieved by calculating a distribution for the importance of frames based on an attention mechanism, facilitating more efficient sampling and analysis.

<p align="center">
  <img src="../images/research/fer-overall_resample_frame.png" width="90%" 
  title="Image Captioning">
</p>

In overview, the model is divided into 2 stages:

Stage 1: The model will generate an attention weight to measure the correlation between frames. Then, a new distribution will be calculated based on this matrix, allowing for more suitable sampling of new frames.


Stage 2: The model will take in the new frame samples and provide the primary prediction results.

<p align="center">
  <img src="../images/research/fer-overall_resample_model.png" width="90%" 
  title="Image Captioning">
</p>

Usage:

1. Frame Sampling: Frames are sampled uniformly from the distribution of original video frames.
2. Feature Extraction: A ResNet backbone is employed to extract features from each sampled frame. This step ensures that relevant information is captured from the frames.
3. Incorporation of Attention Mechanism within Frames: Due to global connectivity limitations, an attention block is introduced. This attention mechanism enhances feature correlation within individual frames.
4. Global Average Pooling (GAP) and Tokenization: Global Average Pooling (GAP) is applied along the spatial dimension. Each frame is collapsed into a single token, which acts as input for subsequent blocks.
5. Temporal Attention Mechanism: Besides typical transformer block outputs, this block generates an attention weight. The attention weight matrix stores the correlation between frames, capturing temporal relationships.
6. Calculation of New Distribution: Utilizing the correlation matrix, a new distribution is computed. This distribution guides the resampling of frames for enhanced temporal understanding.
7. Resampling Frames: Frames are resampled based on the updated distribution. This step ensures that the model captures temporal correlations effectively.
8. Prediction Using Resampled Frames: Primary predictions are made based on the resampled frames.


This multi-stage approach not only enhances the accuracy and efficiency of emotion recognition systems but also renders them indispensable tools across a multitude of fields and applications.

### Electrocardiogram (ECG) classification

<p align="center">
  <img src="{{ site.url }}{{ site.baseurl }}/images/research/ecg_signal.png" width="80%" 
  title="ECG Signal">
</p>
<p align="center">ECG Signal</p>

Early detection and prediction of cardiac anomalies play an important role in the diagnosis and treatment of cardiovascular diseases. In medicine, electrocardiography provides valuable information for the doctors since they can accurately determine what is happening concerning the heart activities. Nevertheless, electrocardiography classification is a non-trivial challenge due to the specialties of these data as well as the reliability of manual data collection methods. This motivates IASLab's members to study electrocardiography signal classification method based on Deep Learning approach to handle data collected from intelligent IoT devices.

### Image/Video Captioning

#### Image Captioning
In today's digital age, images have become the universal language of the internet. Image Captioning - this extraordinary fusion of computer vision and natural language processing has the capacity to bestow machines with the gift of language, enabling them to perceive and describe the intricate tapestry of our visual world in ways that were once the exclusive domain of human understanding.

<p align="center">
  <img src="../images/research/Image Captioning.png" width="90%" 
  title="Image Captioning">
</p>
<p align="center">Image Captioning</p>

The mechanics of image captioning involve a two-fold process: Visual Recognition and Natural Language Generation.
+ First, state-of-the-art deep learning techniques, such as ***Convolutional Neural Networks (CNNs)***, are employed to extract nuanced features from an input image. These features encapsulate information about **shapes**, **objects**, **colors**, and **relationships** within the image.
+ Subsequently, ***Recurrent Neural Networks (RNNs)***, transformer models, or other advanced NLP techniques weave these features into coherent and contextually relevant textual descriptions.

<p align="center">
  <img src="../images/research/Image Captioning - Basic Model.png" width="90%" 
  title="Image Captioning - Basic Model">
</p>
<p align="center">Image Captioning - Basic Model</p>


<!-- Tuan Anh & Tien Nam -->
#### Dense video captioning for short video
With the explosion of social media platforms such as YouTube, Facebook, TikTok, along with the vast amount of short-duration videos being created and shared every day, the demand for models to process and automate video-related workflows, particularly in the field of video understanding, is growing rapidly. The field of Video Understanding comprises various core subtasks such as action recognition and classification, video topic classification, object detection and tracking, video caption generation, and more. Among these tasks, dense video captioning has become one of the most prominent and highly regarded topics due to the challenges it presents and real-world applications.

How does dense video captioning work?
<p align="center">
    <img src="https://i.imgur.com/D5hWrGo.png" width="45%" title="Integrated Architecture" >
</p>

Dense captions generator has many applications in variety of fields: 
- Supporting students in watching and comprehending lecture video content.
- Delivering video content and experience for individuals with visual impairments.
- Assisting users in quickly and efficiently searching, sorting, and filtering video content.
- Summarizing video content and providing concise explanations of videos.
- Enhancing the quality of smart surveillance cameras.

<p align="center">
    <img src="https://i.imgur.com/7PMnEur.png" width="90%" title="Integrated Architecture" >
</p>

<p align="center">
    <img src="https://i.imgur.com/rE2hq2E.png" width="55%" title="Integrated Architecture" >
</p>

Our repository: https://github.com/Tien-Nam-Nguyen/Thesis


### Text-to-Image Generation

Our research team specializes in the exciting field of text-to-image generation. This technology has immense potential across various industries, including e-commerce, advertising, virtual reality, and creative content generation.

Datasets: MS-COCO, ANNA, Multi-modal CelebA-HQ, DeepFashion-MultiModal, ...

Key Features and Capabilities:

1. Advanced Text-to-Image Models: Our team has reproduced and analysis cutting-edge deep learning models that can generate visually coherent and contextually relevant images based on textual input. These models are trained on vast datasets and leverage advanced techniques such as attention mechanisms and generative adversarial networks (GANs) to produce stunning visual representations. Network architectures: DALL-E2, Stable Diffusion, ...
2. Fine-Grained Control: Our models allow fine-grained control over the generated images, enabling users to specify various attributes such as object appearance, background, lighting conditions, and more. This level of control empowers businesses to create custom visuals that align with their brand identity and specific requirements.
3. Scalability and Efficiency: Our research team focuses on developing scalable and efficient models that can handle large-scale text-to-image generation tasks. We optimize our solutions to balance computational resources while maintaining the quality and fidelity of the generated images, ensuring practical application in real-world scenarios.

Use Cases:

1. E-commerce: Generate product images based on textual descriptions, allowing for dynamic and customizable representations of products on e-commerce platforms.
2. Creative Content Generation: Enable artists, designers, and content creators to transform written ideas into vivid visual concepts, bringing stories, illustrations, and designs to life.
3. Virtual Reality and Gaming: Enhance virtual environments and gaming experiences by generating realistic scenes and characters based on textual input, enabling immersive storytelling and world-building.
4. Advertising and Marketing: Create compelling visual advertisements and marketing materials by generating images that accurately depict product features, brand messaging, and customer preferences.
5. Data Visualization: Transform textual data into meaningful visual representations, aiding in data analysis, decision-making, and communication of complex information.

<p align="center">
  <img src="../images/research/text2image-demo-code.png" width="50%" 
  title="text2image-demo-Source code">
</p>

<p align="center">
  <img src="../images/research/text2image-demo-results.png" width="90%" 
  title="text2image-demo-results">
</p>

### Object Detection for the Visually Impaired

Vision is an essential aspect of human life, providing us with the ability to perceive and interact with the world around us. However, visual impairment is a prevalent global issue, affecting a significant proportion of the population. Living with visual impairment poses significant challenges for individuals when it comes to independently navigating their surroundings, both indoors and outdoors.

The objective of this project is to design and deploy an object detection device to assist individuals with visual impairments in their daily lives. This system applies computer vision techniques and image processing to help individuals recognize and locate objects in their surrounding environment. The core components of the system comprise an Intel depth camera, a processor such as a single-board computer/laptop, a microphone, and a headphone. These hardware components work in synergy to enable real-time object detection, obstacle avoidance, and virtual assistant functionalities.

<p align="center">
  <img src="../images/research/visually_impaired_system.png" width="90%" 
  title="Object Detection Visually Impaired">
</p>
<p align="center">The system architecture and modes</p>

Key Features and Capabilities:
1. **Object Finding:** Using voice recognition through the microphone, users can specify the object they wish to find. The system then utilizes the YOLO-World object detection algorithm to identify and locate the desired object in real-time. The results including direction and distance of the object are communicated to the user through text-to-speech conversion. It also incorporates the abilities of obstacle avoiding mode to address the issue that users may encounter obstacles during the process.
2. **Obstacle Avoiding:** The system employs threshold-based object localization within a specific range, typically less than 1 meter. If an obstacle is detected, the system draws a bounding box around it and calculates its exact size. Based on a size threshold, the system then determines whether the obstacle poses a potential harm. The system utilizes text-to-speech conversion to notify the user about the obstacle's position and size.
3. **Assistant:** the Virtual Assistant system provides a range of virtual assistant features. Users can interact with the system to perform various tasks, such as checking the time, quitting the program, changing modes, disabling the program, obtaining weather information, and taking notes. These features aim to assist visually impaired individuals in their daily activities and improve their overall quality of life.

Click [here](https://www.youtube.com/watch?v=G-P9G4ZW4Fg) to see the video demonstrating the system.

### Automatic Slides Generator for Scientific Academic Papers

Presentations are commonly used in the fields of business, education, and research because they can effectively summarize and clarify large amounts of information using visual aids. With the development of deep learning, we aim to create a deep-learning model that can produce presentation slides on demand. This solution involves document summarizing, image and text retrieval, and slide organization to ensure that important components are presented in a suitable format. Our system is designed to help researchers efficiently create presentations on their respective topics.

Datasets: DOC2PPT, SciDuet, PS5K, ...

Key Features and Capabilities:

1. Convert a PDF paper to texts: Our system can convert scientific articles of any length from PDF format to text format by using the GROBID framework, thereby serving subsequent tasks.
2. Generate slides efficiently: Users enter the title of slides. Our system will generate slide contents that match these titles. Users can combine, and edit generated slides
3. Extract graphical elements exactly: Our system uses the pdffigures2 to extract figures and tables that are included in papers. The graphical elements is used in slide generation process.

Use Cases:

1. Researcher: Help the researchers can prepare the presentation quickly and creative.
2. Reader: Enable readers to capture the main idea of the papers.

<p align="center">
  <img src="../images/research/Automatic Slide Generator system architecture.png" width="50%" 
  title="Automatic Slide Generator system architecture">
</p>

<p align="center">
  <img src="../images/research/Slide generation demo.png" width="50%" 
  title="Slide generation demo">
</p>

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

### Medical image segmentation

Medical image segmentation, like a digital scalpel, unveils hidden details in scans to improve diagnoses, treatment, and patient care. While recent deep learning methods using Transformers and U-Net are powerful, they can be computationally expensive. Our MCUnet offers a solution, achieving high accuracy with efficient convolution operations. We introduce three key innovations: CRFBNet for improved skip connections, Multi-Head Output for better predictions, and Consistency Guide Loss for robust multi-head training.

<p align="center">
  <img src="../images/research/MCUnet.png" width="60%" 
  title="Overall Architecture of MCUnet">
</p>
<p align="center">Overall Architecture of MCUnet</p>

<p align="center">
  <img src="../images/research/MCUnetResult.jpg" width="60%" 
  title="Qualitative result">
</p>
<p align="center">Qualitative result</p>

## Others

We always extend our research topic to meet our life needed, if you found a topic is interested, feel free to raise.

### Computer Vision
- Pattern recognition
- Object detection
- etc.

### Time series analysis
- VNPT 4G telecom maintenance
- etc.

