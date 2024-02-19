<p align="center">
  <img src="assets/logo.jpg" height=100>
</p>
<div align="center">

## MotionCtrl: A Unified and Flexible Motion Controller for Video Generation

### <div align="center">👉 MotionCtrl for <b><a href="https://github.com/TencentARC/MotionCtrl/tree/svd">[SVD]</a>, for <a href="https://github.com/TencentARC/MotionCtrl/tree/main">[VideoCrafter]</a></b></div>

[![Paper](https://img.shields.io/badge/Paper-gray)](https://wzhouxiff.github.io/projects/MotionCtrl/assets/paper/MotionCtrl.pdf) &ensp; [![arXiv](https://img.shields.io/badge/arXiv-red)](https://arxiv.org/pdf/2312.03641.pdf) &ensp; [![Project Page](https://img.shields.io/badge/Project%20Page-green
)](https://wzhouxiff.github.io/projects/MotionCtrl/)

🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BSVD&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl_SVD) &ensp; 🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BVideoCrafter&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl)

</div>

---

https://github.com/TencentARC/MotionCtrl/assets/19488619/45d44bf5-d4bf-4e45-8628-2c8926b5954a

---

🔥🔥 We release the codes, [models](https://huggingface.co/TencentARC/MotionCtrl/tree/main) and [demos](https://huggingface.co/spaces/TencentARC/MotionCtrl_SVD) for MotionCtrl on [Stable Video Diffusion (SVD)](https://github.com/Stability-AI/generative-models).

Official implementation of [MotionCtrl: A Unified and Flexible Motion Controller for Video Generation](https://arxiv.org/abs/2312.03641).

MotionCtrl can Independently control **complex camera motion** and **object motion** of generated videos, with **only a unified** model.

### Results of MotionCtrl+SVD

More results are in [showcase_svd](https://github.com/TencentARC/MotionCtrl/blob/svd/doc/showcase_svd.md) and our [Project Page](https://wzhouxiff.github.io/projects/MotionCtrl/).

<div align="center">
    <img src="assets/svd/00_ibzz5-dxv2h.gif", width="300">
    <img src="assets/svd/01_5guvn-0x6v2.gif", width="300">
    <img src="assets/svd/12_sn7bz-0hcaf.gif", width="300">
    <img src="assets/svd/13_3lyco-4ru8j.gif", width="300">
</div>


### Results of MotionCtrl+VideoCrafter

More results are in our [Project Page](https://wzhouxiff.github.io/projects/MotionCtrl/).

<div align="center">
    <img src="assets/hpxvu-3d8ym.gif", width="600">
    <img src="assets/w3nb7-9vz5t.gif", width="600">
    <img src="assets/62n2a-wuvsw.gif", width="600">
    <img src="assets/ilw96-ak827.gif", width="600">
</div>

---

## 📝 Changelog

- [x] 20231225: Release MotionCtrl deployed on ***LVDM/VideoCrafter***.
- [x] 20231225: Gradio demo available. 🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BVideoCrafter&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl)
- [x] 20231228: Provide local gradio demo for convenience.
- [x] 20240115 More camera poses used for testing are provided in `dataset/camera_poses`
- [x] 20240115 Release MotionCtrl deployed on ***SVD***. Codes are in the brach [svd](https://github.com/TencentARC/MotionCtrl/tree/svd) and Gradio Demo is available in 🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BSVD&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl_SVD).
- [ ] Release MotionCtrl deployed on ***AnimateDiff***.

---

## ⚙️ Environment
    conda create -n motionctrl python=3.10.6
    conda activate motionctrl
    pip install -r requirements.txt

## 💫 Inference

- #### Run local inference script

1. Download the weights of MotionCtrl [motionctrl.pth](https://huggingface.co/TencentARC/MotionCtrl/blob/main/motionctrl.pth) and put it to `./checkpoints`.
2. Go into `configs/inference/run.sh` and set `condtype` as 'camera_motion', 'object_motion', or 'both'.
- `condtype=camera_motion` means only control the **camera motion** in the generated video.
- `condtype=object_motion` means only control the **object motion** in the generated video.
- `condtype=both` means control the camera motion and object motion in the generated video **simultaneously**.
3. Running scripts:
        sh configs/inference/run.sh

- #### Run local gradio demo
      python -m app --share



## :books: Citation
If you make use of our work, please cite our paper.
```bibtex
@inproceedings{wang2023motionctrl,
  title={MotionCtrl: A Unified and Flexible Motion Controller for Video Generation},
  author={Wang, Zhouxia and Yuan, Ziyang and Wang, Xintao and Chen, Tianshui and Xia, Menghan and Luo, Ping and Shan, Yin},
  booktitle={arXiv preprint arXiv:2312.03641},
  year={2023}
}
```

## 🤗 Acknowledgment
The current version of **MotionCtrl** is built on [VideoCrafter](https://github.com/AILab-CVC/VideoCrafter). We appreciate the authors for sharing their awesome codebase.

## ❓ Contact
For any question, feel free to email `wzhoux@connect.hku.hk` or `zhouzi1212@gmail.com`.
