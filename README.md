# Joint Training with a Transformer
Decker Krogh  
NLP244 

In this project a single transformer was trained in PyTorch which can solve two tasks at the same time: IOB Slot tagging and relation extraction.

Before main.py can be run you must load the pretrained embeddings with load_embeddings.sh script. 

There's a chance you need to run this first:  
	conda install -c intel mkl_fft

Pip wasn't able to install it so I removed it from the requirements.txt

### Training: 
	python main.py --train --data "hw1_train.csv" --save_model "./joint_trained_model.pt"

### Evaluating: 
	python main.py --test --data "hw1_test.csv" --model_path "./joint_trained_model.pt" --output "./preds.csv"


