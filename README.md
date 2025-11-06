# 1.プロジェクト概要
フライス加工時のセンサーデータを分析し、工具摩耗（tool_wear）を予測する機械学習モデルを構築するプロジェクト。

# 2.使用データ
Kaggle: Milling Tool Wear and RUL Dataset 
[データセットURL](https://www.kaggle.com/datasets/programmer3/milling-tool-wear-and-rul-dataset)

# 3.分析の流れ
1. EDA（データ理解・可視化）
2. 前処理・特徴量エンジニアリング
3. モデル作成
4. モデル評価と考察

# 4.主な結果
LightGBMモデルを用いてMAE=1.829, R²=0.640を達成。  
加工履歴（移動平均）を考慮することでMAE=0.226, R²=0.991まで向上。

# 5.技術スタック
- Python (pandas, matplotlib, seaborn, scikit-learn, lightgbm)
- Jupyter Notebook
- Git / GitHub

# 6.ファイル構成
```
.
├── data
│    ├── processed
│    │    ├── add_plane_vec.csv
│    │    ├── mv_avg_2.csv
│    │    ├── mv_avg_5.csv
│    │    ├── mv_avg_10.csv
│    │    └── mv_avg_20.csv
│    └── raw 
│         └── Milling_Tool_Dataset.csv 
├── notebooks
│    ├── data_processing.ipynb
│    ├── eda.ipynb
│    └── modeling.ipynb
├── outputs
│    ├── data
│    │    └──metrics_summury.csv
│    ├── figures
│    │    ├── data_proccesing
│    │    │    ├── add_features_pairplot.png
│    │    │    ├── add_mv_avg_2.pairplot.png
│    │    │    ├── add_mv_avg_5.pairplot.png
│    │    │    ├── add_mv_avg_10.pairplot.png
│    │    │    └── add_mv_avg_20.pairplot.png
│    │    ├── eda
│    │    │    ├── all_feature_corr_heatmap.png
│    │    │    ├── all_feature_hitplot.png
│    │    │    ├── all_feature_lineplot.png
│    │    │    └── all_feature_pairplot.png
│    │    └── modeling
│    │         ├── add_pvec_importances_histplot.png
│    │         ├── lightgbm_feature_importances_histplot.png
│    │         ├── mv_avg20_acoustic_lineplot.png
│    │         ├── raw_acoustic_lineplot.png
│    │         ├── raw_add_pvec_result_histplot.png
│    │         └── raw_mvavg_reasult_histplot.png
│    └── reports
│         └── report.md
├── src
├── LICENSE
├── README.md
└── requirements.txt
```

# 7.環境
Python 3.13.5  
Install dependencies:
```bash
pip install -r requirements.txt

##Skills Demonstrated
-Data preprocessing (pandas, numpy)
-Visualization (matplotlib, seaborn)
-Machine_learning (scikit-learn,LightGBM)
-SQL + Python integration

 8a799f4 (Add initial project structure and EDA notebook template)
 