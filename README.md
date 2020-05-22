# SupCos
Validate unfinished

This repo is for implementation of:
- Supervised Contrastive Learning: [Paper](https://arxiv.org/abs/2004.11362)

## Dependencies
- PyTorch 1.4.0 
- Torchvision 0.5.0
- CUDA 10.0, cuDNN 7.5.1

## How to use
Please be careful for the `batch_size` option: adjust it depending on your GPU memory.
Learning rate may not be optimized that much... (Processing)

** Baseline model training and validation (ResNet50) **
```
python main_baseline.py --batch_size 128 --lr 0.75 --epochs 600
```

** Supervised Contrastive model: Stage 1(embedding + projection) training and validation **
```
python main_embed.py --batch_size 128 --lr 0.75 --epochs 500
```

** Supervised Contrastive model: Stage 2(classifier) training and validation **
```
python main_embed.py --batch_size 128 --lr 1 --epochs 100
```

## Augmentation
[AutoAugment](https://arxiv.org/abs/1805.09501) by default. you can change it to manual by giving option:
```
--augment Basic
```

## References
[1] Supervised Contrastive Learning: [Paper](https://arxiv.org/abs/2004.11362)
[2] AutoAugment: [Github](https://github.com/4uiiurz1/pytorch-auto-augment)