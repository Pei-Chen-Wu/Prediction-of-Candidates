# Prediction-of-Candidates
## Learning skills
* DataFrame 資料處理
* AlexNet
* VGG
* FaceNet
* MTCNN
* SVC

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

## Data 說明
* 103-All_concat.csv : 103年度里長全台縣市競選
* 103photo_1024.csv : 103年度里長照片名稱與競選結果（長寬皆小於1024者）
* 103-more_than_1_concat.csv ： 103年度里長全台縣市競選（競選人數超過一人）
其他依此類推

## Code 說明
* Data processing.ipynb : 針對 raw text data 分析
* Data processing 2.ipynb ： 針對照片進行分析
* AlexNet.ipynb ： 單純照片與label輸入
* VGG.ipynb : 單純照片與label輸入
* FaceNet.ipynb : 使用 FaceNet 開發人臉識別系統 example (包含MTCNN,FaceNet,SVC) , 識別五位名人照片與名字配對
  * Keras FaceNet 預訓練模型 (88 MB) 下載網址 ： https://drive.google.com/open?id=1pwQ3H4aJ8a6yyJHZkTwtjcL4wYWQb7bn  
