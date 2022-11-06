
![visitors](https://visitor-badge.glitch.me/badge?page_id=deforum_sd_local_1.5_repo&left_color=green&right_color=red)

# Deforum Stable Diffusion (V0.5) Local Version

This is a Local implementation of Deforum Stable Diffusion V0.5, supports json settings file.
Supports all Stable Diffusion Models, Including v1-5-pruned.ckpt

**Example Animated Video**
*these examples videos are generated using Deforum 0.5 and SD  Check Point 1.5 (v1-5-pruned.ckpt). Also the settings for these examples are alvailable in "examples" folder*
![example](examples/race.gif)


**Videos Generated using this Script**
Watch these videos in youtube, these were generated using Deforum Stable Diffusion V0.5. I built this script primarily to generate these kind of Videos.

<p float="left">
  <a href='https://www.youtube.com/watch?v=f6asZSdUvOg'><img src="https://img.youtube.com/vi/f6asZSdUvOg/0.jpg" width="400" /></a>
  <a href='https://www.youtube.com/watch?v=YNYMaLc8HBY'><img src="https://img.youtube.com/vi/YNYMaLc8HBY/0.jpg" width="400" /></a>
  <a href='https://www.youtube.com/watch?v=qkFsSCP5cXg'><img src="https://img.youtube.com/vi/qkFsSCP5cXg/0.jpg" width="400" /></a>
  <a href='https://www.youtube.com/watch?v=CfqsKcbdCFU'><img src="https://img.youtube.com/vi/CfqsKcbdCFU/0.jpg" width="400" /></a>
</p>

This script is based on the Colab code by deforum (v0.5). I have tested it on ***Ubuntu 22.04*** + ***Nvidia RTX 3090 ti***



## Installation

You can use an [anaconda](https://conda.io/) environment to run this on your local machine:

```
conda create --name dsdv0.5 python=3.8.5 -y
conda activate dsdv0.5
```

And then cd to the cloned folder, run the setup code.

```
python setup.py
```

## Manually download 3 Model Files

*Most of these files will be automatically downloaded during your first run. If not, you can download them manually.*

* You need to get the `v1-5-pruned.ckpt` file and put it on the `./models` folder. It can be downloaded from [HuggingFace](https://huggingface.co/runwayml/stable-diffusion-v1-5/).
* Additionally, you should put `dpt_large-midas-2f21e586.pt` on the `./models` folder as well, [the download link is here](https://github.com/intel-isl/DPT/releases/download/1_0/dpt_large-midas-2f21e586.pt)
* There should be another extra file `AdaBins_nyu.pt` which should be downloaded into `./pretrained` folder, [the download link is here](https://cloudflare-ipfs.com/ipfs/Qmd2mMnDLWePKmgfS8m6ntAg4nhV5VkUyAydYBp8cWWeB7/AdaBins_nyu.pt)


## How to use it?
The running command should looks like this:
```
python run.py --settings "./settings/animation_settings.json" --generate_video true
```

*The output results will be available at `./output` folder.*

Required variables & prompts for Deforum Stable Diffusion are set in the json file found in settings folder and I have also provided the settinngs for the example videos in *"example"* folder.



**Thanks to**
- **[Stable Diffusion](https://github.com/CompVis/stable-diffusion) by Robin Rombach, Andreas Blattmann, Dominik Lorenz, Patrick Esser, Björn Ommer and the [Stability.ai](https://stability.ai/) Team.**
- **[K Diffusion](https://github.com/crowsonkb/k-diffusion) by [Katherine Crowson](https://twitter.com/RiversHaveWings).** 
- **Notebook by [deforum](https://discord.com/invite/upmXXsrwZc)**


Enjoy!