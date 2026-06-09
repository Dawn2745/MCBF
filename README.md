# Before the Turn: Investigating Motion Cues Preceding Speech in Dyadic Interaction <!--, INTERSPEECH 2026-->

## Overview

While traditional conversational AI models rely on reactive acoustic and linguistic boundaries, they inherently lag behind human intention. In face-to-face dialogues, interlocutors physically prepare for speech well before vocalization occurs. 

This repository presents a **systematic analysis to determine the effect of continuous kinematics on predictive lead times**. We evaluate a **Transformer architecture** on **InterAct 3D skeletal data** by systematically varying observation windows and predictive lead times across diverse, multi-case dyadic scenarios.

<p align="center">
  </p>

### Key Findings
* **Asynchronous Timelines:** Communicative intent operates on independent physical timelines across different body parts.
* **3.0s Early Warning:** **Upper-body signals** enable stable predictive intent horizons up to **3.0 seconds prior to speech onset**.
* **Intent-Driven Kinematics:** Proactively **turn-claiming** involves a **1.5s preparatory build-up** of motion diversity, whereas defending the floor (**floor-holding**) triggers an **explosive kinetic burst** right at the speech collision boundary.

This work establishes asynchronous multimodal coordination as a core governing principle of proactive and naturalistic human-agent interaction.


## Dataset
The following corpora is required for our work
- InterAct

Please download the [dataset](https://huggingface.co/datasets/leohocs/interact) first.
- raw bvh is in `InterAct_Public/Raw_Body_Motions_BVH`
- raw audio is in `InterAct_Public/Raw_Audios_WAV`



## Running the sample code

Create the conda environment and install the dependencies
```
conda create -n your_env_name python=3.9.23
conda activate your_env_name
cd MCBF/analysis
python -r requirement.txt
```
###  Motion Onset Detection
The trainig code is provided in the "train" directory.
Remember to change `base_dir` to your directory.

```
cd ../train
python -r requirement.txt
python run_exp_part_3.py
```

### Decision-Time

Remember to change `base_dir` to your directory.

The sample training code is like:
```
python training_part_4.py --ref_bvh InterAct_Public/Raw_Body_Motions_BVH/20231119_001_052.bvh  --manifest manifest_shifted_tau_0.0.csv --baselines speaker_norm_6D_fps30_baselines.json
```

## Citation(preparing)
If you find the code useful in your research or work, please consider citing our paper:
<!--```
@inproceedings{,
  title={Before the Turn: Investigating Motion Cues Preceding Speech in Dyadic Interaction},
  author={Ying-Hsuan Huang, Woan-Shiuan Chien, Huan-Yu Chen and Chi-Chun Lee},
  booktitle={Proc. Interspeech 2026},
  year={2026}
}
```-->
