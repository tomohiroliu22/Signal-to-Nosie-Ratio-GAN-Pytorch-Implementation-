# Signal-to-Noise Ratio Generative Adversarial Network

This project describes the SNRGAN model, which introduce 4 noise into real source domain, real target domain, fake source domain, and fake target domain, respectively. This project is modified from junyanz/pytorch-CycleGAN-and-pix2pix project. 

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
