<h1 align="center"> RS-GNN : Robust and stable learning via Logarithmic Norm Regularization</h1>
<p align="center"> <a href="https://github.com/SarathMohanIITD" target="_blank id="website">Sarath Mohan </a>, <a href="https://scholar.google.com/citations?user=MRJqKywAAAAJ&hl=en&oi=ao" target="_blank id="website">Vipul Kumar Singh </a>, <a href="https://sites.google.com/view/sandeepkr/home" target="_blank id="website">Sandeep Kumar</a></p>
<p align="center">  <a href="https://misn.iitd.ac.in/" target="_blank id="website">MISN Lab , IIT Delhi </a>



A PyTorch implementation of "Robust and stable learning via Logarithmic Norm Regularization" 

## Abstract 
- Graph Neural Networks (GNNs) have demonstrated remarkable performance across
numerous application domains due to their ability to capture the potential of
the interconnectedness of data. As GNN is getting adopted in the industry and
government organizations, adversarial attacks on GNN have become a significant
threat that can affect the overall performance of the learner. Additionally, as
the depth of models increases, their performance often deteriorates significantly
due to over-smoothing of the node features. The current defense techniques to
handle both bottlenecks require significant computational resources, lack scalability,
and rely on specific architectural configurations. In this work, we formulate a
joint framework for graph denoising and GNN training along with logarithmic
norm regularization on the product of layer-wise activations. The proposed use
of logarithmic norm regularization aids in bounding the difference between the
embeddings obtained from the original graph signal and the perturbed graph. The
proposed frameworks are solved efficiently by leveraging block majorization-
minimization, graph learning, and alternate minimization. The developed iterative
algorithm is efficient and provably convergent. Simulation results on real datasets
demonstrate the efficacy of the proposed method over state-of-the-art methods. The
method also provides a new paradigm for the training of deep GNNs.

## Requirements
See that in https://github.com/DSE-MSU/DeepRobust/blob/master/requirements.txt

## Installation
To run the code, first you need to install DeepRobust:
```
pip install deeprobust
```
Or you can clone it and install from source code:
```
git clone https://github.com/DSE-MSU/DeepRobust.git
cd DeepRobust
python setup.py install
```

## Run the code
After installation, you can clone this repository or you can use the demo notebook here [COLAB](https://github.com/SarathMohanIITD/RS-GNN/blob/main/RS_GNN.ipynb)
```
https://github.com/SarathMohanIITD/RS-GNN
cd RS-GNN
!python train.py --two_stage y --bound 0.5 --seed 30 --dataset citeseer  --attack meta --ptb_rate 0.25 --epochs 200 --epochs_pre 400 --alpha 1.0  --gamma 1.0 --beta 0.3 --lr_optim 1e-2 --lr 1e-3
```
<!-- [colab]: <https://colab.research.google.com/assets/colab-badge.svg>
[RS-GNN]: <https://github.com/SarathMohanIITD/RS-GNN/blob/main/RS_GNN.ipynb> -->

## Acknowledgements
The code is based on :
- DeepRobust [(https://github.com/DSE-MSU/DeepRobust)](https://github.com/DSE-MSU/DeepRobust)
- [Pro-GNN](https://github.com/ChandlerBang/Pro-GNN)
- [RWL-GNN](https://github.com/Bharat-Runwal/RWL-GNN)


