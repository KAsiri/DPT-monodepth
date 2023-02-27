### Modified From: Vision Transformers for Dense Prediction https://github.com/isl-org/DPT to work on Google Colab notebooks

### Setup 


1) clone the repo to a new Colab notebook

    ```
    !git clone https://github.com/KAsiri/DPT-monodepth.git
    ```

2) Download the model weights and place them in the `/content/DPT-monodepth/weights` folder:

    ```
    !wget -P /content/DPT-monodepth/weights https://github.com/intel-isl/DPT/releases/download/1_0/dpt_hybrid-midas-501f0c75.pt 
    ```
    ```
    !wget -P /content/DPT-monodepth/weights https://github.com/intel-isl/DPT/releases/download/1_0/dpt_large-midas-2f21e586.pt
    ```

Monodepth:
- [dpt_hybrid-midas-501f0c75.pt](https://github.com/intel-isl/DPT/releases/download/1_0/dpt_hybrid-midas-501f0c75.pt), [Mirror](https://drive.google.com/file/d/1dgcJEYYw1F8qirXhZxgNK8dWWz_8gZBD/view?usp=sharing)
- [dpt_large-midas-2f21e586.pt](https://github.com/intel-isl/DPT/releases/download/1_0/dpt_large-midas-2f21e586.pt), [Mirror](https://drive.google.com/file/d/1vnuhoMc6caF-buQQ4hK0CeiMk9SjwB-G/view?usp=sharing)

  
3) Set up dependencies: 

    ```
    !pip install -r /content/DPT-monodepth/requirements.txt
    ```

### Usage 

1) Place one or more input images in the folder `/content/DPT-monodepth/input`.

2) Run a monocular depth estimation model:

    ```
    !python /content/DPT-monodepth/run_monodepth.py
    ```
    
3) The results are written to the folder `/content/DPT-monodepth/output_monodepth`.


### Citation

```
@article{Ranftl2021,
	author    = {Ren\'{e} Ranftl and Alexey Bochkovskiy and Vladlen Koltun},
	title     = {Vision Transformers for Dense Prediction},
	journal   = {ArXiv preprint},
	year      = {2021},
}
```

```
@article{Ranftl2020,
	author    = {Ren\'{e} Ranftl and Katrin Lasinger and David Hafner and Konrad Schindler and Vladlen Koltun},
	title     = {Towards Robust Monocular Depth Estimation: Mixing Datasets for Zero-shot Cross-dataset Transfer},
	journal   = {IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI)},
	year      = {2020},
}
```

### Acknowledgements

This is a modified copy from:
Vision Transformers for Dense Prediction https://github.com/isl-org/DPT 
This repository contains code and models for our paper:

Vision Transformers for Dense Prediction
René Ranftl, Alexey Bochkovskiy, Vladlen Koltun

Our work builds on and uses code from [timm](https://github.com/rwightman/pytorch-image-models) and [PyTorch-Encoding](https://github.com/zhanghang1989/PyTorch-Encoding). We'd like to thank the authors for making these libraries available.

### License 

MIT License 
