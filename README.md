Research Question
The NLP and NLU space is rapidly evolving and becoming more competitive. Companies and open source groups are making models more powerful while simultaneously becoming easier to use. Just this week, OpenAi's GTP3 language prediction model became available to the general public.

The goal of this notebook is to analyze the sentiment of Tweets for a given search term using NLP algorithms. This notebook serves as lightweight proof of concept for a program that could monitor Tweets in real-time. Many similar commercial products (Brandwatch, Lexalytics. Critical Mention) exists that monitors Twitter to identify overall brand sentiment, changes in sentiment, and potential customer facing issues.

The inputs for this notebook are Tweets collected at runtime. The output high-level analysis of transformations.

The following predictions will be made using pre-trained models:

Emotion Detection
Sentiment Analysis
Twitter Trained Sentiment Analysis
Fake News Classification
Spam Classification
Toxic Language Detections
Sarcasm Classification
Keyword Extraction
Named Entity Recognition

This notebook uses the John Snow NLU library and requries Java 8 and Pyspark. Setup for a Colab notebook is below. Additional configurations can be found here: https://nlu.johnsnowlabs.com/docs/en/install


```# Set-up Colab Environment to use John Snow Lab NLU
!wget https://setup.johnsnowlabs.com/nlu/colab.sh -O - | bash
import os
! apt-get update -qq > /dev/null   
# Install java
! apt-get install -y openjdk-8-jdk-headless -qq > /dev/null
os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-8-openjdk-amd64"
os.environ["PATH"] = os.environ["JAVA_HOME"] + "/bin:" + os.environ["PATH"]```
