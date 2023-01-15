# ogbg-code2

This repository includes the scripts for GNN baselines for `ogbg-code2` dataset.
This code requires Pytorch Geometric version>=`2.0.2` and torch version>=`1.10.1`.

**Note (Feb 24, 2021)**: The older version `ogbg-code` is deprecated due to prediction target (i.e., method name) leakage in input AST. `ogbg-code2` (available from `ogb>=1.2.5` ) fixes this issue, where the method name and its recursive definition in AST are replace with a special token `_mask_`. The leaderboard results of `ogbg-code` and `ogbg-code2` are *not* comparable. 

## Training & Evaluation

```
# Run with default config.
# $GNN_TYPE and $FILENAME are described below.
python main_pyg.py --gnn gat
```
