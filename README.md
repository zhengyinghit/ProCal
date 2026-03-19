# ProCal
Code for our paper "ProCal: Probability Calibration for Neighborhood-Guided Source-Free Domain Adaptation"

## Prerequisites:
- python == 3.9.20
- pytorch == 2.4.0
- torchvision == 0.19.0
- numpy, scipy, sklearn, PIL, argparse

## Dataset:

Please manually download the datasets from the official websites, and modify the path of images in each '.txt' under the folder './data/'.

## Training:

- Train model on the source domain
    ```python
    python image_source.py --trte val --output ckps/source/ --gpu_id 0 --dset office-home --max_epoch 50 --s 0 
    ```
	
- Adaptation to other target domains
    ```python
    python train_ProCal.py --dset office-home --gpu_id 0 --s 0 --max_epoch 15 --interval 15 --output_src ckps/source/ --output ckps/ProCal/
    ```

## Acknowledgment

This project is based on SHOT ([paper](https://proceedings.mlr.press/v119/liang20a.html), [code](https://github.com/tim-learn/SHOT)) and AaD ([paper](https://arxiv.org/abs/2205.04183), [code](https://github.com/Albert0147/AaD_SFDA)), thanks for their excellent works.

## Contact
If you have any questions or suggestions, please contact zhengyinghit@outlook.com. Thanks for your attention!
