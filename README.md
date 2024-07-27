# stan-r-bayes-statistical-modeling-python

# 環境構築（フロムスクラッチの手順）
1. condaで適当な仮想環境を作る。python versionのみ指定する。
    * ディレクトリに入る
    * `conda deactivate`
    * `conda create -n stanbayes -c conda-forge python=3.11` (*1)
    * (optional) `conda info --envs`：仮想環境一覧確認
    * `conda activate stanbayes`
    
1. 各種インストール
    * `conda install "pymc>=5.11"` 
    * `pip install japanize-matplotlib`
    * `conda install seaborn`

1. `pip install jax jaxlib numpyro` 
    * -> requirements.txt参照
    * しかしこれでまだスピードアップしたわけではなさそう。結構時間がかかってる気がする。
1. `conda install -n [環境名] ipykernel --update-deps --force-reinstall`

1. requirements.txtのアップデート
```
conda list > requirements.txt
```

### 補足
1. pymc installation : https://www.pymc.io/projects/docs/en/stable/installation.html 