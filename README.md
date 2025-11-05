# プロジェクト概要
CNC加工時のセンサーデータを分析し、工具摩耗（tool_wear）を予測する機械学習モデルを構築。

# 使用データ
Kaggle: Multi-Sensor CNC Tool Wear Dataset  
[データセットURL](https://www.kaggle.com/datasets/ziya07/multi-sensor-cnc-tool-wear-dataset)

# 分析の流れ
1. EDA（データ理解・可視化）
2. 前処理・特徴量エンジニアリング
3. モデル作成（LightGBM）
4. モデル評価と考察

# 主な結果
LightGBMモデルを用いてMAE=1.844, R²=0.640を達成。  
加工履歴（移動平均）を考慮することでMAE=0.240, R²=0.991まで向上。

# 技術スタック
- Python (pandas, matplotlib, scikit-learn, lightgbm)
- Jupyter Notebook
- Git / GitHub

# ファイル構成
data/
    raw/
        Milling_Tool_Dataset.csv
    processed/
        mv_avg_2.csv
        mv_avg_5.csv
        mv_avg_10.csv
        mv_avg_20.csv
        processed_data.csv 
notebooks/
    eda.ipynb
    data_processing.ipynb
    modeling.ipynb

src/            

outputs/
    report_en.md
    report.md

# 環境
Python 3.x  
Install dependencies:
```bash
pip install -r requirements.txt

##Skills Demonstrated
-Data preprocessing (pandas, numpy)
-Visualization (matplotlib, seaborn)
-Machine learning (scikit-learn)
-SQL + Python integration

 8a799f4 (Add initial project structure and EDA notebook template)
 