# Anime Generator App

## Overview

This application combines the power of GPT-3.5, an advanced language model developed by OpenAI, with the "Anythingv5" model in the Stable Diffusion Pipeline to create high-quality, 2D, anime style manga panels from textual descriptions. The app further enhances the created manga panels by adding speech bubbles with the character's dialogue.

## This app is equipped with several textual inversion models, specifically "EasyNegative", "verybadimagenegative", and "badhandv4", which play a vital role in transforming textual descriptions into visual elements. The Stable Diffusion Pipeline also incorporates LoRa (Low-Rank Adaptation) weights to fine-tune the diffusion model to display manga-style art.

## Prerequisites

A CUDA-compatible GPU is necessary, as the pipeline uses CUDA for computation.
The data type is set as torch.float16 for memory efficiency. Ensure your system supports this data type.
OpenAI API Key for GPT-3.5 model.
Features
GPT-3.5 Textual Descriptions
The app interfaces with the GPT-3.5 model via the OpenAI API to generate textual descriptions for a manga scene. The GPT-3.5 model acts as a manga artist describing the scene's background, the looks, actions, expressions, and positions of each character using only adjectives.

## The input for this feature is a JSON message with the keys plotline and character.

## Image Generation

The app uses the image_creator function to generate an image from the combined descriptions using the Stable Diffusion Pipeline. The pipeline takes in the description prompts and uses them to generate corresponding images, depicting a high-quality, 2D, anime style masterpiece with highly detailed faces and backgrounds.

## Speech Bubbles

After generating the images, the create_speech_bubbles function is used to add dialogues to the manga panels. The function takes an image, dialogues for each character, and the panel number as inputs, and draws speech bubbles with the corresponding dialogues onto the image.
