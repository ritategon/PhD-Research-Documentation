---
up: index
title: Covers Processing with Aya Vision
description: A Colab notebook that analyses video game covers using Cohere's Aya Vision model.
categories:
  - methodology
  - tools
  - visual-corpus
colab_link: https://colab.research.google.com/drive/1hcVObtSbnr7VNKP9Gw5KrNFSQY6jZSjt?usp=sharing
image: /images/notebooks/covers-preview.jpg
tags:
  - notebook
  - colab
  - aya-vision
  - cohere
  - computer_vision_analysis
---

# Covers Processing with Aya Vision

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1hcVObtSbnr7VNKP9Gw5KrNFSQY6jZSjt?usp=sharing)

This notebook uses the **Cohere API**, specifically the [`c4ai-aya-vision-32b`](https://docs.cohere.com/page/aya-vision-intro) model, to conduct a comprehensive analysis of video game cover images as part of the wider [[Multimodal  Corpus]] in this PhD project.

It contributes to the analysis of Herakles' visual representation in modern media by extracting structured information from a [[set of video games]].

---

## Purpose

The objective of this notebook is to automate the extraction of descriptive and semantic features from visual inputs. The model returns detailed outputs on:

- Persons, objects, clothing
- Landscapes and environments
- Mood and emotion
- Labels and symbols
- Estimated geography
- Transcribed text (if present)
- Cohesive narrative synthesis

This aligns with the research focus on [[Herakles in Video Games]] and supports the [[Quantitative Analysis]] and [[Qualitative Analysis]] of the visual corpus.

---

## Workflow Summary

### 1. Installation  
Installs the `cohere` library, required to access the Cohere API.

### 2. Authentication  
The notebook authenticates using an API key.  
**Note:** You must insert your personal API key from [Cohere Dashboard](https://dashboard.cohere.com/).

### 3. Image Preprocessing  
Images are loaded from local paths using `IPython.display` and encoded via `base64`.

### 4. Query to Aya Vision  
The prompt and image are sent to the Aya Vision endpoint.  
A custom message prompt guides the model to return structured information.

### 5. Response Handling  
The API returns a JSON structure which is parsed and formatted into readable text output.

---

## Libraries Used

- [`cohere`](https://pypi.org/project/cohere/)
- `IPython.display` (Jupyter environment)
- `base64` (image encoding)
- `requests` (for API communication)

---

##  Input

The current input image path:  
`/content/01 - The return of Heracles 1983.jpg`

---

## Output

The model returns:

- A rich narrative summary of the image
- Key entities and symbolic objects
- Contextual location inference
- Transcribed text and its layout
- Emotional tone and interpretive layer

These results feed into both the [[Appendix C: List of Covers of Video Games]] and the ongoing [[Comparative Analysis]] with ancient sources.

---

##  Related Pages

- [[Methodology]]
- [[Visual Corpus]]
- [[Herakles in Video Games]]
- [[Tools]]
- [[Data Analysis Notebooks]]

---

_Source repository: [ritategon/PhD-Research-Documentation](https://github.com/ritategon/PhD-Research-Documentation)_

## Locations

| Name | Coordinates | Description | Certainty | Pleiades ID | Heracles Context |
|------|-------------|-------------|-----------|-------------|------------------|