---
title: Building a AWS Machine Learning Course Interactive Dashboard
excerpt: A user-friendly dashboard application for exploring machine learning course videos
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/9ff33e130373914fe50742562984fb89.png
---

## **Business Scenario**

The training organization has 46 videos covering various Machine Learning topics. The project aims to develop a user-friendly dashboard that enables students to easily find relevant video content based on their search queries.

## **Techniques**

- video and audio processing: ffmpeg
- video editing and manipulation: MoviePy
- speech-to-text conversion: OpenAI Whisper
- text processing and analysis: NLTK
- Keyphrase extraction: model (`ml6team/keyphrase-extraction-kbir-inspec`) from the Hugging Face Transformers library. This model is likely based on a BERT-like architecture and is trained to identify important keyphrases within text.
- Data handling: Pandas
- Data visualization: WordCloud, Bokeh

## **Workflow**

### **1. Data Acquisition and Preprocessing**

- Video to Audio Conversion: Convert the MP4 video files to MP3 audio files using `ffmpeg` or `moviepy`. 
- Speech-to-Text Transcription: Use the OpenAI Whisper model to transcribe the audio files into text and save the transcripts as text files. 
- Create DataFrame: Load the transcripts into a Pandas DataFrame, associating each transcript with its corresponding video name. 
- Data Cleaning and Normalization: Apply text normalization techniques (lowercasing, lemmatization, removing non-ASCII characters, URLs, emojis, punctuation, numbers, and stop words) to clean and prepare the transcripts for further analysis. 
- Add Metadata: Extract video module information and calculate text length to enrich the DataFrame.

### **2. Keyphrase Extraction**

- Initialize Keyphrase Extractor: Load the pre-trained keyphrase extraction model (`ml6team/keyphrase-extraction-kbir-inspec`). 
- Extract Keyphrases: Apply the keyphrase extractor to the normalized transcripts to identify important keyphrases for each video. 
- Refine Keyphrases: Perform further refinement on extracted keyphrases, such as replacing common abbreviations with their full forms and lemmatizing.

### **3. Data Organization and Analysis**

- Create Keyword Dictionary: Build a dictionary mapping keyphrases to their corresponding video names to facilitate search functionality. 
- Create Keyword DataFrame: Convert the keyword dictionary into a Pandas DataFrame for easier analysis and manipulation. 
- Calculate Keyword Frequency: Determine the frequency of each keyphrase across all videos. 
- Filter Keyphrases: Apply criteria based on keyword length, character count, and frequency to filter out less relevant or redundant keyphrases.

### **4. Dashboard Creation and Visualization**

- Create Visualization Components: Use Bokeh to build interactive visualizations, such as bar charts to show video count and average text length by module, word clouds to display frequent keyphrases, annular wedges to represent topic distribution within modules, and a horizontal bar chart to visualize text length for each video. 
- Create Filterable Table: Implement a searchable and filterable table using Bokeh to display keyphrases and their associated videos. 
- Assemble Dashboard Layout: Arrange the visualization components and table within a Bokeh layout to create the final dashboard. 
- Display Dashboard: Show the dashboard using the `show()` function from Bokeh, allowing users to interact with the visualizations and search for video content using keyphrases.

## Functionalities
**a. Compare modules**
<img src="/assets/obsidian/9ff33e130373914fe50742562984fb89.png" />

**b. WordClouds**
<img src="/assets/obsidian/4d20f74d52dc9077546a24ea7fac69a4.png" />

**c. List Main Topics**
<img src="/assets/obsidian/59648cee6091ee5ac9ff17a0991252f5.png" />

**d. Compare Text Length**
<img src="/assets/obsidian/78e5cc67d524c36f1bf7a6aeeaff5b99.png" />

**e. Search Keywords**
<img src="/assets/obsidian/7ae0b4e2ef4b89b970dd70b0d83d3963.png" />

<img src="/assets/obsidian/1b98ce2e347cc95aaa935f2851c29dea.png" />

## Demo

[Web App](https://aws-ml-course-dashboard.onrender.com/main)

<iframe width="560" height="315" src="https://www.youtube.com/embed/hYbHdYCohWQ?si=3uTvhieM1lDCDNs0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


