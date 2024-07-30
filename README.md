#  Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension

Thank you very much for your contribution! I encountered the same problem as [#14 ](https://github.com/stanford-oval/storm/issues/14)when running the command
```shell
-- python -m scripts.run_writing --input-source console --input-path ../FreshWiki/topic_list.csv --engine gpt-4 --do-polish-article --remove-duplicate. 
```
The error is
```shell
ValueError: Expected 2D array, got 1D array instead: array=[]. Reshape your data either using array.reshape(-1, 1) if your data has a single feature or array.reshape(1, -1) if it contains a single sample. 
```
Then I checked what you said a bunch of  
```shell 
root : ERROR : Error occurs when searching query xxx: 'hits'?
``` 
and found that mine is 
```shell
Error occurs when searching query Taylor Hawkins musical influences: 'url' 
Error occurs when searching query Taylor Hawkins musical background: 'url'
Error occurs when searching query Music inspirations of Taylor Hawkins: 'url'
```  
Can you help me check it?

Code for the COLING2022 paper "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension"
[[Paper]](https://aclanthology.org/2022.coling-1.357/)

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
We follow the unified evaluation framework (raganato framework) for WSD. You can download the dataset [here](http://lcl.uniroma1.it/wsdeval/home) and unpack it in the data folder.
## Train the WSD Model on the Dataset
If you want to train your own model you just have to run the following command in the KELESC folder:
```shell
python model/train.py
```
## Evaluation
If you want to evaluate the model on a dataset, just run the following command in the KELESC folder:
```shell
python model/predict.py --ckpt <kelesc_checkpoint.ckpt> --dataset-paths data/WSD_Evaluation_Framework/Evaluation_Datasets/semeval2007/semeval2007.data.xml 
```
The ```--dataset-paths``` can be modified. For example, change  ```/semeval2007/semeval2007.data.xml``` to ```/semeval2013/semeval2013.data.xml```. The predictions will be saved in the folder ```predictions``` with the name ```<dataset_name>_predictions.txt```.
## Citation
Please cite our paper if you find it helpful.
```
@inproceedings{,
    title = "Word Sense Disambiguation with Knowledge-Enhanced and Local Self-Attention-based Extractive Sense Comprehension",
    author = "Guobiao Zhang and 
      Wenpeng Lu and
      Xueping Peng and
      Shoujin Wang and
      Baoshuo Kan and
      Rui Yu",
    booktitle = "Proceedings of the 29th International Conference on Computational Linguistics",
    year = "2022",
}
```
## Acknowledgement
Parts of the code are modified from [ESC](https://github.com/SapienzaNLP/esc). We appreciate the authors for making ESC open-sourced.

