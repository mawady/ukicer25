# Advancing Assessment Practices in CS Education through AI-Generated Visual Test Cases

##  Citation

```ACM reference
Mohamed Elawady. 2025. Advancing Assessment Practices 
in CS Education through AI-Generated Visual Test Cases. 
In UK and Ireland Computing Education Research Conference 
(UKICER 2025), September 04–05, 2025, Edinburgh, United Kingdom. 
ACM, New York, NY, USA, 1 page.
https://doi.org/10.1145/3754508.3754538
```

## Demo

- Image Classification Validator:
  - Used models: ResNet18, ConvNextV1-Tiny
  - Pre-trained weights: ImageNet
  - Function: Upload an AI-generated image to see top-3 predictions from classification models with probabilities.
  - [[Google Colab](https://colab.research.google.com/drive/1Ma1eVp-A6btT7yLZzguuNXeAK0Grceuc?usp=sharing)]
  - [[Gradio Demo](https://f9c97e2b56721bb5c5.gradio.live/)] - temporary share
  - [[HF Spaces Demo](https://huggingface.co/spaces/mawady-uni/ImgClsValid)]  - permanent share

- Image Detection Validator:
  - Used models: YOLOv8n, YOLOv12n
  - Pre-trained weights: COCO
  - Function: Upload an AI-generated image to view the top three predictions from detection models, including their probabilities, along with the corresponding bounding boxes for each model.
  - [[Google Colab](https://colab.research.google.com/drive/1VMFIkbg4yrbRtlx6G0jmAOZUBnaqpfT_?usp=sharing)]
  - [[Gradio Demo](https://4f249791ef35fa7222.gradio.live/)] - temporary share
  - [[HF Spaces Demo](https://huggingface.co/spaces/mawady-uni/ImgDetValid)] - permanent share

## Visual Test Cases (cats)

### Prompt

- generate realistic image (cat in room) and write bounding box coordinates of cat within the image to be used later to compare with object detection models. don't show annotation box over the generated image.

### Google - Gemini 2.5 Flash

- Data Folder (images): [./imgs/gemini-2.5-flash/](./imgs/gemini-2.5-flash/)
- Link: <https://gemini.google.com/>
- Discussion: Capable of generating images; however, automatic bounding box generation for object detection is not supported.

### OpenAI - ChatGPT GPT5

- Data Folder (images and detection information in json format file): [./imgs/chatgpt-gpt5/](./imgs/chatgpt-gpt5/)
- Link: <https://chatgpt.com/>
- Discussion: Successfully generated images with bounding box information and text descriptions in JSON format. Further example generation is constrained by paywall restrictions.

### Anthropic - Claude Sonnet 4

- Link: <https://claude.ai/chat/>
- Discussion: Unable to automatically generate images or annotation metadata for object detection. However, capable of creating and running an annotation application that allows manual image upload, bounding box drawing, and exporting annotations in multiple formats (COCO, YOLO, Pascal VOC).

### Microsoft - M365 Copilot GPT5

- Link: <https://m365.cloud.microsoft/chat/>
- Discussion: Very slow in execution

### StabilityAI - Stable Diffusion 2.1

- Links:
  - <https://huggingface.co/spaces/stabilityai/stable-diffusion>
  - <https://huggingface.co/stabilityai/stable-diffusion-2>

- Discussion: Unable to generate annotation metadata for object detection since the model is limited to text-to-image generation. The outputs are less realistic, and only basic prompt text such as 'cat in room' can be used.

### Black Forest Labs - FLUX.1-dev

- Links:
  - <https://huggingface.co/spaces/black-forest-labs/FLUX.1-dev>
  - <https://huggingface.co/black-forest-labs/FLUX.1-dev>
- Discussion: Cannot generate annotation metadata for object detection as it is restricted to text-to-image generation. Outputs tend to be less realistic (mainly focusing on the same body pose) and rely on simple prompts such as 'cat in room,' though performance is superior to Stable Diffusion 2.1.

### Craiyon - DALL·E mini

- Link: <https://huggingface.co/spaces/dalle-mini/dalle-mini>
- Discussion: One of the earliest open-source text-to-image generation models, lacking object detection metadata. The outputs are highly unrealistic.
