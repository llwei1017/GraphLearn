
# Count-GNN
We provide the implementaion of Count-GNN model on Small,Large,MUTAG dataset.

The repository is organised as follows:
- data/: due to the limitation of upload file size, data/ only contains MUTAG data .
- Count_GNN/: contains our model.



## Package Dependencies

* tqdm
* numpy
* pandas
* scipy
* tensorboardX
* torch >= 1.3.0
* dgl == 0.4.3post2

## Running experiments

To run _train.py:
- python _train.py --model EDGEMEAN --predict_net FilmSumPredictNet --gpu_id 0 --emb_dim 4 --ppn_hidden_dim 12 --predict_net_recurrent_steps 3 --reg_loss MAE --weight_decay_film 0.0001 --bp_loss MAE --predict_net_hidden_dim 128 --batch_size 1024 --epochs 250 --max_npv 4 --max_npe 3 --max_npvl 2 --max_npel 2 --max_ngv 28 --max_nge 66 --max_ngvl 7 --max_ngel 4 --pattern_dir ../data/MUTAG/patterns --graph_dir ../data/MUTAG/raw --metadata_dir ../data/MUTAG/metadata --save_data_dir ../data/MUTAG --save_model_dir ../dumps/MUTAG/EDGEMEAN-FilmSumPredictNet1.1 --share_emb False &

To run evaluate.py:
- python evaluate.py ../dumps/MUTAG1000/EDGEMEAN-FilmSumPredictNet1.1

