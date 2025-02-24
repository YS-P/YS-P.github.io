---
layout: post
title:  "Quantization"
author: 2han
featured: true
categories: [ quantization, climate change ]
image: assets/images/2_windpower.jpg
rating: 4
---

Nowadays, AI is everywhere, and people are using it in their daily lives. The AI market is expanding rapidly, along with its technology.

AI requires a vast amount of data. Companies like Google, Amazon, and Meta have enormous databases. To keep these databases cool, a large amount of water is needed, and they also emit a significant amount of co2.

<div style="text-align: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/2_datacenter.png" alt="walking" style="width: 70%; max-width: 500px;">
  <figcaption style="font-size: 0.3em;">Source: https://www.reuters.com/markets/carbon/global-data-center-industry-emit-25-billion-tons-co2-through-2030-morgan-stanley-2024-09-03/</figcaption>
</div>

> A boom in data centers is expected to produce about 2.5 billion metric tons of carbon dioxide-equivalent emissions globally through the end of the decade, and accelerate investments in decarbonization efforts, according to Morgan Stanley research.

The International Energy Agency (IEA) reported in a September 2022 publication that data centers consume approximately 1% of global electricity demand and account for 0.3% of global CO2 emissions.

Greenhouse gases, including CO₂, accelerate global warming, so we need a solution to prevent this. One possible solution is **Quantization**.

## Quantization in Machine Learning
Quantization is a method of converting weights and activation functions into smaller bit representations, which enhances model performance and efficiency.

The main goal of quantization is to minimize the impact on model accuracy while reducing the model size and lowering computational complexity.

Normally, models based on PyTorch or TensorFlow consist of 32-bit floating-point (float32) representations. Through quantization, we can convert these to smaller bit representations, such as 16-bit floating-point (float16) or 8-bit integers (int8). This approach helps reduce memory usage and computational complexity.

However, the quantization process can lead to information loss, which may result in reduced accuracy. Therefore, we must be aware of this trade-off and find the optimal balance between accuracy and computational cost.

## Quantization Experiment
Now, let's verify the effects of quantization through an actual experiment.

#### Dataset
[COCO dataset 2017]  
https://cocodataset.org/#download

#### Task
- Get the model and use LiteRT (formerly TensorFlow Lite) to quantize the model
- Choose the following three configurations (weights only):  
  ■ float32  
  ■ float 16  
  ■ int8  

#### Backbone Model
[Mask R-CNN with Inception ResNet V2 backbone]
https://www.kaggle.com/models/tensorflow/mask-rcnn-inception-resnet-v2
- Overview
    Mask R-CNN with Inception Resnet v2 (using regular Convolutions instead of Dilated ones). Trained on COCO 2017 dataset (Synchronous SGD across 8 GPUs) with batch size 16 (trained on images of 1024x1024 resolution). 

#### Result
![objectdetection](https://github.com/user-attachments/assets/38cc1853-a7fb-4bd9-ac38-4577fdd77803)
- Significant Enhancement on Model Size and Inference Time for all configurations
- Poor mean Average Precision

#### Additional Result
<img width="1094" alt="스크린샷 2025-01-16 오전 2 21 11" src="https://github.com/user-attachments/assets/d7fb6bea-9cf0-463b-a8eb-10fa2f2a3797" />

#### Analysis
As you can see, after quantization, the model size has decreased. In particular, the int8 model shows a significant difference compared to other models, being nearly five times smaller than the original model. The inference time is also noticeably shorter than that of other models.

Additionally, you can confirm from the results that the quantized model achieves similar detection accuracy compared to the other models.

## Further Discussion
As you can see, the Mean Average Precision (mAP) is extremely low across all models. This is unusual. Upon debugging the code, it was found that the low accuracy resulted from a misalignment between the x-coordinates and y-coordinates of the ground truth and predictions. A proper method to align these coordinates needs to be explored in the future.


---
<a href="https://github.com/YS-P/Quantization_RESNETv2" target="_blank">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" width="30" alt="GitHub">
  View on GitHub
</a>