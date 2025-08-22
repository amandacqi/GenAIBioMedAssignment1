<h1>02741/02541/11481/11781-A Assignment1: Finetuning ProGen2 on Green Fluorescent Protein Design</h1>

<h2>ProGen2</h2>

ProGen2 is a foundation model for protein design. For detailed information, please check [paper](https://www.cell.com/cell-systems/fulltext/S2405-4712(23)00272-7)

In this assignment, you'll learn how to finetune the pretrained ProGen2 model on a specific protein family, e.g., green fluorescent protein.

![image](./GFP.png)


<h2>Environment</h2>
The dependencies can be set up using the following commands:

```ruby
conda create -n progen python=3.9.16 -y 
conda activate progen 
pip install torch==2.7.0 torchvision==0.22.0 torchaudio==2.7.0 --index-url https://download.pytorch.org/whl/cu128
python -m pip install transformers
```

<h2>Downloading Pretrained models</h2>

```ruby
mkdir pretrained_model
mkdir models
mkdir pretrained_model/progen2-small
cd pretrained_model/progen2-small
wget https://storage.googleapis.com/sfr-progen-research/checkpoints/progen2-small.tar.gz
tar -xvzf progen2-small.tar.gz
```

<h2>Finetuning</h2>

We already provided the full training pipeline. What you need to do 
is finish the TODO modules in the current code. 
Please **Don't change the other parts, especially the seed and the hyperparameters we give notes**

<h2>Training</h2>

```ruby
python train.py
```

<h3>Design</h3>

```ruby
python inference.py
```