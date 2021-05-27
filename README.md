# OpenHGNN
This is an open-source toolkit for Heterogeneous Graph Neural Network(OpenHGNN) based on [DGL](https://github.com/dmlc/dgl). We will integrate SOTA models of heterogeneous graph.

[Test Version]For now, we just release some models for some researchers to run the experiments.

### Keys

- Easy-to-Use: OpenHGNN provides easy-to-use interfaces for running experiments with the given models and datasets. TODO: [Feature]AutoML & hyper-parameter search.
- Extensibility: User can define customized task/model/dataset to apply new models to new scenarios.
- Efficiency: The backend dgl provides efficient APIs.

#### Why OpenHGNN

##### Relation with [dgl](https://github.com/dmlc/dgl)

OpenHGNN is a high-level package built on top of DGL; it will not cover efficient implementation of low-level components in C++.

##### Relation with [OpenHINE](https://github.com/BUPT-GAMMA/OpenHINE)

| Package  | Heterograph structure | Models                            | Efficiency  | Others                                     |
| -------- | --------------------- | --------------------------------- | ----------- | ------------------------------------------ |
| OpenHINE | write by our own      | Most embedding methods            | Inefficient | ---                                        |
| OpenHGNN | dgl.heterograph       | Most graph neural network methods | Efficient   | Better Extensibility, Better Encapsulation |

To avoid reinventing the wheel, we use the dgl as our backend. So we build the new toolkit OpenHGNN and more models will be integrate into it. OpenHINE will not continue updating.

![image](./docs/source/image-001.jpg)

## Get Started

#### Requirements and Installation

- Python  >= 3.6
- [PyTorch](https://pytorch.org/get-started/locally/)  >= 1.7.1
- [DGL](https://github.com/dmlc/dgl) >= 0.6.1

#### Running an existing baseline model on an existing benchmark dataset

```python
python main.py -m model_name -d dataset_name -t task_name
```

It is under development, and we release it in a nightly build version. For now, we just give some new models, such as HetGNN, NSHE, GTN, MAGNN, RSHN.

### Some models

- [HetGNN](https://github.com/BUPT-GAMMA/OpenHGNN-DGL/tree/main/openhgnn/output/HetGNN)[KDD2019] for node classification and link prediction
- RSHE[ICDM2019] for entity classification
- [GTN](https://github.com/BUPT-GAMMA/OpenHGNN-DGL/tree/main/openhgnn/output/GTN)[NeurIPS 2019] for node classification
- HAN[WWW 2019] for node classification
- NSHE[IJCAI2020]
- MAGNN[WWW2020]

### Contributors

GAMMA LAB [BUPT]: Tianyu Zhao, Cheng Yang, Xiao Wang, Chuan Shi

BUPT: Jiahang Li

DGL Team: Quan Gan, Jian Zhang
