# ML
previous work

For hw2:

一、嘗試改變自變數 x=GrLivArea，試做後發現效果不如原本好，故目前維持原本的8個自變數

二、mean_absolute_error #若使用此loss function則添加隱藏層前的rmse僅4.91，效果不錯，但添加隱藏層後的rmse不佳
若使用squared_hinge,mean_squared_logarithmic_error 在添加隱藏層前相當不準
故維持原本的mean_squared_error

三、加hidden layer時，將神經元數量往上加(如加到35或50)，改善效果並不明顯，此部分可能尚待重複試驗

四、sigmoid跟tanh的效果不好，

在原本基礎上新增一個hidden layer (relu) 可使rmse下降，但若再新增一層反而使效果變差

For TF3_DNN:

https://www.kaggle.com/chrisfilo/fruit-recognition?select=Carambola 我找了kaggle上的圖檔 選取其中 AppleA 與 Tamotoes 的圖檔資料進行分辨的驗證

作業的目的是分辨番茄與蘋果的圖像

令人驚訝的是 在使用cnn神經層之後，預測的準確率奇高無比，接近1

我認為可能的原因是: 訓練圖檔與測試圖檔都過於相似 單純

我認為我這次找的圖檔不好，但也側面證明了機器學習在簡單情況下分辨事物的高準確率。

FOR TF5:

目前決定先用上課建置之模型試試看，分析壽司郎的留言評價。

因為採用google評論，確知有星等評價可反映正負意向。

取留言共20條，1-3星為負評，4-5星為好評。

研究結果：

經由RNN模型預測後的準確率僅七成。

遇到的問題:
例如: 服務生 說話 超級 快 很 像 複讀 機器
這句負評，因為沒有"負面"詞語，導致模型無法辨認
同理: 覺得 食材 都 縮水 了 厚度 也 比 以前 薄
及:炸 南瓜 除了 沒有 南瓜 香甜 的 味道 ，麵衣 相當 的 油膩 
"縮水"與"油膩"亦沒有被識別為負面詞語，導致模型錯誤判斷以上2句為正評
