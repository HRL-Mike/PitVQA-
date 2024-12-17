<div align="center">

<samp>
<h2> PitVQA++: Vector Matrix-Low-Rank Adaptation for Open-Ended Visual Question Answering in Pituitary Surgery </h1>
</samp> 

---
| **[[```arXiv```](<https://arxiv.org/>)]** | **[[```Paper```](<https://link.springer.com/>)]** | **[[```Colab Demo```](<https://github.com/>)]**|
|:-------------------:|:-------------------:|:-------------------:|
    
Conference / Journal name
---

</div> 

## PitVQA++ Network

<div align='center'>
<img src='https://github.com/mobarakol/PitVQA/blob/main/assets/model_archi_3.png' width=750>
</div>

## Open-ended PitVQA Dataset

Our Open-ended PitVQA dataset comprises 25 videos of endoscopic pituitary surgeries from the The National Hospital of Neurology and Neurosurgery in London, United Kingdom. All videos were annotated for the surgical phases, steps, instruments present and operation notes guided by a standardised annotation framework, which was derived from a preceding international consensus study on pituitary surgery workflow [16]. Annotation was performed collaboratively by 2 neurosurgical residents with operative pituitary experience and checked by an attending neurosurgeon. 
We extracted image frames from each video at 1 fps and removed any frames that were blurred or occluded. Ultimately, we obtained a total of 101,803 frames, with the videos of minimum and maximum length yielding 2,443 and 7,179 frames, respectively. We acquired frame-wise question-answer pairs for all the types of the annotation. Overall, there are 745,972 question-answer pairs from 101,803 frames, which is around 8 pairs for each frame.
This work is an extension of our <a href="https://github.com/mobarakol/PitVQA/tree/main">previous work</a>.

<div align='center'>
<img src='https://github.com/mobarakol/PitVQA/blob/main/assets/pitvqa_dataset_2.png' width=650>
</div>

<div align='center'>
<img src='https://github.com/mobarakol/PitVQA/blob/main/assets/Dataset_Annaotation_Classes.png' width=650>
</div>

## How to Download PitVQA Dataset
Please download full [PitVQA dataset](https://doi.org/10.5522/04/27004666) from UCL RDR portal. 
The original videos were taken and preprocessed from [MICCAI PitVis challenge](https://rdr.ucl.ac.uk/articles/dataset/PitVis_Challenge_Endoscopic_Pituitary_Surgery_videos/26531686)

The dataset split for training and validation as below:<br>

train_seq = ['01', '03', '04', '05', '07', '08', '09', '10', '11', '14',
             '15', '16', '17', '18', '19', '20', '21', '22', '23', '25']
                     
val_seq = ['02', '06', '12', '13', '24']


## Training Command:
For EndoVis18-VQA dataset:
```
python main.py --dataset=endo18 --epochs=60 --batch_size=64 --lr=0.00002
```

For PitVQA dataset:
```
python main.py --dataset=pit24 --epochs=60 --batch_size=64 --lr=0.00002
```
## Acknowledgement
The implementation of PitVQA relies on resources from <a href="https://github.com/salesforce/BLIP">BLIP</a>, <a href="https://github.com/huggingface/transformers">Huggingface Transformers</a>, <a href="https://github.com/rwightman/pytorch-image-models/tree/master/timm">timm</a> and our previous work [SurgicalGPT](https://github.com/lalithjets/SurgicalGPT). We thank the original authors for their open-sourcing.

## Citation
If you use this code for your research, please cite our paper.

```
Add reference
```
