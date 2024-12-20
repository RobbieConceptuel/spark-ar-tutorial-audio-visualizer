# Spark AR - Audio Visualizer

**Note: As of January 2025, Meta Spark AR Studio has been officially discontinued by Meta Platforms Inc.**  

## What is Spark AR Studio?  
Spark AR Studio is software developed by Meta Platforms Inc. that allowed users to create interactive augmented reality (AR) experiences.  
It has been widely used to create popular AR filters for Instagram, Facebook, and other social platforms.  
With its intuitive tools and strong community, Spark AR played a key role in the rise of augmentism, a trend that blends art and technology to enhance our perception of the world through digital experiences.

### The End of Spark AR Studio  
In January 2025, Meta Platforms Inc. decided to end the development and support of Spark AR Studio, marking the conclusion of a platform that significantly contributed to the growth of augmented reality in social media.

---

A heartfelt thank you to everyone who contributed to Spark AR Studio, its resources, and the advancement of augmentism.  
Your creativity, passion, and dedication have left a lasting impact on the world of augmented reality.  

---

using the software Meta Spark Studio

This tutorial is an entry for the [2020 Developer Circles Community Challenge](https://developercircles2020.devpost.com/) hosted by Facebook.

**Regional Winner** 🏅

## Overview :mag:

Welcome in this Meta Spark AR Studio tutorial . 
In this project, we will learn how to make an **audio visualizer** using the audio features in Meta Spark AR.
This is a tutorial for beginner.

At the end of the tutorial you will learn how to make an Audio Visualizer like this:

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/AudioVisualizer_FinalResult.jpg" width="300">

This tutorial will cover :
* importing the 3d object
* Make it react to audio using the Patch Editor

In this tutorial I’m using the version 99 of Meta Spark AR Studio.

## Why You Should Use Meta Spark AR ? :bulb:

With more than 400,000 creators from 190 countries, Meta Spark AR is the **largest platform for mobile AR** . 
Over 1.2 million AR effects where published on Facebook and Instagram .

  <img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/sparkarinsights.png" width="500">


### **This is just the beginning**

We are still in the early days! Every update is a surprise with new features.

With or without code, Meta Spark AR Studio enhances your creativity and expand your digital creative skills. 
A powerful software to create astonishing Augmented Reality effects.


### **The best tool to reach a large audience!**


<a href="https://sparkar.facebook.com/ar-studio/download/">
  <img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/sparkarlogo.svg" width="200">
</a>

[Download Meta Spark AR Studio](https://sparkar.facebook.com/ar-studio/download/)

## Videos :clapper:

A quick [Walkthrough Video](https://www.youtube.com/embed/1JrhmM9n-BU) of the tutorial.

<a href="https://www.youtube.com/embed/1JrhmM9n-BU">
  <img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/thumbnailTutorial.png" width="200">
</a>


The following video is a step-by-step video tutorial.
It contains and show all the process described in this tutorial.


<a href="https://www.youtube.com/embed/1JrhmM9n-BU">
  <img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/thumbnailVideoTutorial.png" width="500">
</a>

#### [Step-by-step Video](https://youtu.be/1BcGiDr2FO4)

## Getting Started :walking:

For this project we need :
* [Download Meta Spark AR](https://sparkar.facebook.com/ar-studio/download/)
* 3D model in the folder 3D-model [link to model](https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/3D-model/audioBar.fbx)
* Having Meta Spark AR Player installed in your phone [link to Meta Spark AR Player](https://sparkar.facebook.com/ar-studio/learn/downloads/)


To start this tutorial, you need to **download** the software Meta Spark AR Studio and **open** it.
You also need the 3D model '**audioBar.fbx**' in the folder '3D-model'.
We will see the audio nodes in the patch editor and use it.

## Setting up the scene

Let's start our project by :
1. Opening the software
2. New Project
3. Choose Plane Tracking

Once our project is opened.
Let's **drag and drop** the 3D model in the project **then drag the object in the placer**.

Select the audioBar in your scene and change the scale value to 0.1 on your right like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/ScaleaudioBar.png" width="200">

When done, duplicate the audioBar and change the position of the second audioBar value to 0.2 on the X axis.
like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/PositionaudioBar2.png" width="200">

Repeat this step until you have **8 audioBar**.
The scene on your left top of the screen should look like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Scene.png" width="200">

### Material
Now let's create the materials we gonna apply on the 3d object (audioBar).
For this project I will create **8 materials** with different colors.

To apply a material :
* select the cube inside the audioBar
* on the right, create a material
* select your material on the left side of your screen

Like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/ApplyMaterial.png" width="600">

Now that you have your material, we can improve it by :
* changing the 'Shader Type' and choose 'Physically-Based'
* changing the colour

Import an environment texture :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Import_EnvironmentTexture.png" width="200">

The material should look like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Material.png" width="250">

## Make the 3D object react to audio :running:
### Edit Properties
The features we are using are only available for Instagram.
We have to disable Facebook as a platform.
For this we go under : Project > Edit Properties > Uncheck Facebook

Like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/EditProperties.png" width="500">

### Audio Analyzer :musical_keyboard:

Now that your scene is placed, we open the Patch Editor :
| View > Show/Hide Patch Editor

It will open the Patch Editor.

In your scene : 
1. drag and drop the Microphone in your Patch Editor.
2. Right Click in the patch editor and select under Audio the Audio Analyzer
3. link the microphone to the Audio Analyzer ( Microphone to Audio)

The Audio Analyzer is an element that provide us the ability to separate the audio into 8 different channels.
The frequencies goes from 0Hz to 12'000Hz.

Info about the Audio Analyzer :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/AudioAnalyzer_Info.png" width="300">

### Scale the 3D object
Select your audioBar, on the right of your screen you have to active the scale by clicking the arrow.
Here :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Scale_PatchEditor.png" width="300">

Right click in the Patch Editor and add a 'Transition' element.
Change the values of the transition element to make it look like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/TransitionPatch.png" width="300">

Link the Audio Analyzer > Transition > audioBar '3D Scale'

### Add a Speaker :speaker:
Now we have add a speaker to use it as the output of the audio.
In you scene :
* click on 'Add Object' and add a speaker
* select your Speaker
* click on the arrow under Audio 

like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/ActivateSpeaker.png" width="300">


Link the first output of your Audio Analyzer to the Speaker output (yellow element) :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Transition_1element.png" width="600">

Repeat the step with the audioBar2

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Transition_2elements.png" width="600">

Repeat these steps for all your audioBar objects.

Your patch should look like this :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Screenshot_SparkAR_Audio_Visualizer.png" width="600">

## Preview and Upload :rocket:

Now that we are finished ;
we can preview our effect to your **Meta Spark AR Player** app or send **to your Instagram** account :

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Preview_effect.png" width="300">

We're ready to upload !

On bottom of your screen :
* click Upload and Export
* Follow the process of uploading a filter to your account

<img src="https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer/blob/main/images/Upload_and_Export.png" width="200">



Link to the project on GitHub : https://github.com/RobbieConceptuel/spark-ar-tutorial-audio-visualizer


*Made with :sparkling_heart: by Robbie Conceptuel - Updated in 2024*
