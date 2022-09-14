#  Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension

Code for the COLING2022 paper "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension"
[[Paper]]()

## Environment
- 
- 
- 
- 


## Data Preparation
You can download the dataset [here](http://lcl.uniroma1.it/wsdeval/home) and put it in the data folder.
## Run the WSD Model on the Dataset
We recommend use cuda to accelerate the inference. Make sure you have generated the necessary files and put the dataset file in the `data/` directory.
```shell
CUDA_VISIBLE_DEVICES=0 python run_model.py
```
The command will test the model on the whole dataset and generate a log file for further evaluation.
## Evaluation
After you get the log file, you can evaluate it with the following command on various metrics. 
```shell
python parse_log.py --model bert
```
## Citation
Please cite our paper if you find it helpful.
```
@inproceedings{,
    title = "",
    author = "",
    booktitle = "Proceedings of the 29th International Conference on Computational Linguistics",
    year = "2022",
}
```


