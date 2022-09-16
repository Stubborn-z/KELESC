#  Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension

Code for the COLING2022 paper "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension"
[[Paper]]()

## Environment
- black=21.5b2
- nlp=0.4.0
- nltk=3.4.5
- numpy=1.21.2
- pandas=1.3.5
- python=3.7.12
- pytorch=1.8.0
- pytorch-lightning=0.9.0
- tqdm=4.64.0
- transformers=3.2.0
- wandb=0.12.12


## Data Preparation
You can download the dataset [raganato framework](http://lcl.uniroma1.it/wsdeval/home) and put it in the data folder.
## Train the WSD Model on the Dataset
If you want to train your own model you just have to run the following command in the KELESC folder:
```shell
python esc/train.py
```
The command will test the model on the whole dataset and generate a log file for further evaluation.
## Evaluation
After you get the log file, you can evaluate it with the following command on various metrics. 
```shell

```
## Citation
Please cite our paper if you find it helpful.
```
@inproceedings{,
    title = "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension",
    author = "Guobiao Zhang, Wenpeng Lu1, Xueping Peng, Shoujin Wang, Baoshuo Kan, Rui Yu",
    booktitle = "Proceedings of the 29th International Conference on Computational Linguistics",
    year = "2022",
}
```


