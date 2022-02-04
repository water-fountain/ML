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
