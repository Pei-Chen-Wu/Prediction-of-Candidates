# Prediction-of-Candidates
## Learning skills
* DataFrame 資料前處理
* 資料分析
* AlexNet
* VGG
* FaceNet
* MTCNN
* SVC
* factor_analyzer
* 斷詞資料庫 ( word2vec , jieba , ckip)
* BERT取文意向量


## 每週進度
* 11/9 : 
  * raw data分析
  * 未來方向探討

* 11/16 :
  * 資料問題
  * 長寬分佈圖
  * final資料總數
  * 照片前處理
  * Resnet model
 
* 11/26 :
  * CNN 介紹
  * model(LeNet,AlexNet,VGG) 介紹
  * model(LeNet,AlexNet,VGG) 成果
  * Data _ 把一人競爭拿掉
  * Face classification

* 11/30 :
  * 使用 FaceNet 開發人臉識別系統 example

* 12/7 :
  * 整理僅兩人競選
  * 分析（連任 政治 性別....）
  * factor_analyzer
  * 使用 FaceNet 開發人臉識別系統（2人且連任拿掉）

* 12/17 :
  * 訓練分類器 （Text）
    - 全加
    - 連任
    - 號碼
    - ...
  * AlexNet : 測試raw photo (2人一組且拿掉連任）
 
* 12/21 :
  * 107data探討
    * 確認特徵與103一樣
  * 斷詞資料庫
    * LDA
    * word2vec
    * jieba (中國斷詞庫）
    * ckip (台灣中研院)
   
* 12/28 : 
  * 學歷分為六大類 

* 1/11 :
  * 學歷手動調整
  * 學歷分析
  * 經歷政見：	
    * 詞性分類
    * 實體辨識
  * BERT取文意嵌入
    * 介紹
    * 範例
    * 實作

* 1/18 :
  * BERT取文意嵌入實作
  * 放入SVM分析

* 1/26 :
  * BERT特徵_數值意義
  * 探討整組無連任組
    * 比較組（維持特徵維度768與句長512）
    * max_lengh = 64 , 128 , 256
    * token_ids數量 分佈圖
    * 混合max_lengh
    * 輸出降維
    * 自建NN
  

## Data 說明
* 103-All_concat.csv : 103年度里長全台縣市競選
* 103photo_1024.csv : 103年度里長照片名稱與競選結果（長寬皆小於1024者）
* 103-more_than_1_concat.csv ： 103年度里長全台縣市競選（競選人數超過一人）
* 103-two_compare.csv : 103年度兩人競爭
* facenet_train.csv ： 103年度兩人競爭且連任拿掉（欲丟入facenet model的data）
* factor.csv ： 欲丟入 factor_analyzer 的text data
* bfi.csv : factor_analyzer的範例data (28人格特質)
* 107factor_continue.csv : 107 text data factor(兩人競爭 包含連任)
* 107factor_no_continue.csv ： 107 text data factor(兩人競爭 不包含連任)
* 103_e_p.csv : 經歷和政見的pos與ner（詞性分類 與 實體辨識）

其他依此類推


## Code 說明
* Data processing.ipynb : 針對 raw text data 分析
* Data processing 2.ipynb ： 針對照片進行分析
* Data processing 3.ipynb ： 整理僅兩人競選 並分析
* AlexNet.ipynb ： 單純照片與label輸入
* VGG.ipynb : 單純照片與label輸入
* FaceNet.ipynb : 使用 FaceNet 開發人臉識別系統  (包含MTCNN,FaceNet,SVC) , 識別五位名人照片與名字配對
   * example ： Keras FaceNet 預訓練模型 (88 MB) 下載網址 ： https://drive.google.com/open?id=1pwQ3H4aJ8a6yyJHZkTwtjcL4wYWQb7bn  
   * 後面為 facenet_train.csv facenet_test.csv 所得之照片分類
* test_facenet.ipynb : 使用raw照片
* factor_analyzer.ipynb ： 多因子特徵分析 
  * 包含範例 https://vincentarelbundock.github.io/Rdatasets/datasets.html
  * 103資料factor.csv
* 分類器.ipynb : 將現有六特徵丟入分類器
  * SVM(RBF)
  * Multi-layer Perceptron (MLP)
  * XGBoost
* Education.ipynb : 將學歷分為六大類
  - 小學以下
  - 國初中
  - 高中高職
  - 專科
  - 大學
  - 研究所以上
* experience_politics.ipynb : 透過BERT 取出經歷與政見文意
