# FedVHA

A lightweight federated learning research codebase for comparing FedAvg-style aggregation, FedVHA, and several baselines under non-IID client splits.

## Supported Experiments

- Datasets: CIFAR-10, MNIST, SVHN
- Models: VGG16, LeNet
- Algorithms:  FedVHA

## Setup

Install the core dependencies:

```bash
pip install -r requirements.txt
```

## Example Commands

FedVHA on CIFAR-10 with VGG16:

```bash
python -u main.py --dataset cifar10 --model VGG16 --algorithm fedvha --beta 0.1 --data_root ../../data --log_dir ./log_/cifar10_vgg16_beta=0.1_fedvha
```

FedVHA on MNIST with LeNet:

```bash
python -u main.py --dataset mnist --model LeNet --algorithm fedvha --beta 0.1 --data_root ../../data --log_dir ./log_/mnist_lenet_beta=0.1
```

FedVHA on SVHN with VGG16:

```bash
python -u main.py --dataset svhn --model VGG16 --algorithm fedvha --beta 0.1 --data_root ../../data --log_dir ./log_/svhn_vgg16_beta=0.1
```

## Notes

Datasets, checkpoints, logs, and generated figures are intentionally excluded from this repository. Put datasets outside the repo and pass their location with `--data_root`.
