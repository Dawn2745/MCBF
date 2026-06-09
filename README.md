# Before the Turn: Investigating Motion Cues Preceding Speech in Dyadic Interaction, INTERSPEECH 2026

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

## Citation
If you find this code useful, please consider citing:
