# Toward Cell Nuclei Precision between OCT and H&E Images Translation using Signal-to-Noise Ratio Cycle-consistency
This project is used to implement the SNRGAN in  **Toward cell nuclei precision between OCT and H&E images translation using signal-to-noise ratio cycle-consistency**.

Link: https://www.sciencedirect.com/science/article/pii/S016926072300490X?dgcid=rss_sd_all

This project describes the SNRGAN model, which introduce 4 noise into real source domain, real target domain, fake source domain, and fake target domain, respectively. This project is modified from junyanz/pytorch-CycleGAN-and-pix2pix project. 


## Model Introduction
The SNRGAN introduces 4 noises to increase the robustness of the image translation and also improve the quality of the converted images. This framework is utilized in OCT and H&E image translation, which can not only prevent the artifacts generated in fake OCT images but also enhance the translation accuracy for H&E images.

## Dataset format
You should check out the size of A domain images are the same with B domain image.

```
./[your own path]/dataset
----/trainA   % A domain training set image file [png]
----/trainB   % B domain training set image file [png]
----/testA    % A domain testing set image file [png]
----/testB    % B domain testing set image file [png]
```

## Model Training

```
python train.py --dataroot ./[your own path]/dataset --name [your model name] --model cycle_gan --noise1 'YES' --noise2 'YES' --noise3 'YES' --noise4 'YES' 
```

## Model Testing

```
python test.py --dataroot ./[your own path]/dataset --name [your model name] --model cycle_gan --noise1 'YES' --noise2 'YES' --noise3 'YES' --noise4 'YES'
```

## Citation
Please cite this bibtex if you use this repository
```
@article{liu2023toward,
  title={Toward cell nuclei precision between OCT and H\&E images translation using signal-to-noise ratio cycle-consistency},
  author={Liu, Chih-Hao and Fu, Li-Wei and Chen, Homer H and Huang, Sheng-Lung},
  journal={Computer Methods and Programs in Biomedicine},
  pages={107824},
  year={2023},
  publisher={Elsevier}
}
```
