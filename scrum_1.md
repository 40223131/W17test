# 由 scrum_1 組員40223102、40223104所寫的JavaScript canvas 繪圖概念與指令討論(未完成)

說明Brython協同繪圖模式下
與JavaScript canvas繪圖對應的相關概念與可用的程式

JavaScript是弱類型語言，一種基於對象和事件驅動的腳本語言，可以直接嵌入HTML文檔中，並可以動態裝載、編寫，可以控制瀏覽器直接對文本和圖形進行處理。

然而無論是遊戲或是圖片，我們都希望都能在網頁中呈現出來，不過在這裡我們網頁的編寫程式是使用JavaScript，而我們在課堂中所用的python要轉換成JavaScript，必須使用Brython來轉換。

當我們要使用JavaScript canvas繪圖，並在網頁中顯示繪製結果，也要使用Brython來轉換。

![](https://copy.com/KsWlBQzpWfivPd7u)


# 由 scrum_1 組員40223102所寫的專案一考試報告
在模數和傳動比给定的情况下，小齒輪的齒數 越小，大齒輪齒數 以及齒數和( + )也越小，齒輪機構的中心距、尺寸和重量也减小。
因此設計時希望把 取得盡可能小。
  但是對漸開線標準齒輪，其最少齒數是有限制的。如下公式所示:
2/(sin壓力角)^2=過切最小齒數
  所以當壓力角為20度時，代入公式  2/(sin 20)^2
2/(sin 20)/(sin 20)=17
即壓力角為20度時齒輪的最小齒數為17。
  在應用以上的原理，並用程式繪製出互相嚙合的齒輪。


  首先下載2015scrum解壓縮後，複製到v槽裡面，用leo開啟cp_project，進入index編輯。如下圖所示:

![](https://copy.com/bjyqrip9R1MHNFWZ)
midx=400在x軸方向移動400。

![](https://copy.com/GWxK8i71Vtx8o46J)
紅框的部分midx=400+3*rp，原本設定midx=400+ra了時後圖示會出現干涉，後來將原本的400+ra改為400+3*rp(節圓半徑)，因為大齒輪直徑為小齒輪的兩倍，故我們尺寸為這樣設定。

![](https://copy.com/cBwDGk8uOaucHWhR)
更改完成後，可以看得出來大小齒輪已嚙合。

# 由 scrum_1 組員40223104所寫的專案一考試報告
這次作業我負責的是利用Creo繪製3D齒輪，要在leo當中設定參數，然後讓程式計算齒數、模數、壓力角等數據。
![](https://copy.com/rHurBZ9gs1DaLxiF)
↑定義所要設定的變數名稱，例如module是模數的名稱。

![](https://copy.com/qoxkqis9jjfE7KLS)
↑除了設定名稱之外，還要做好其他的定義，要讓每個定義的變數都有個對應的名稱。

↓完成程式編寫後上傳到近端，並在creo的頁面上輸入網址。
![](https://copy.com/riJW6UwyAghYk6rf)

輸入之後就會開始計算，並呈現出計算後的齒輪模樣。
![](https://copy.com/yKZY8anbXsa0cM3M)

一開始我並不知道該怎麼完成分配到的任務，還好有組長的教導才能順利的完成這次的作業。



# 由 scrum_1 組員40223104所寫的七齒輪嚙合考試報告
這次我負責的地方是七個齒輪嚙合中，第二齒的部分。
首先開啟ger.leo →進入index 
在第一齒輪下方打上
第2齒數:cinput type=text name=N1和br /
如下圖所示↓
![](https://copy.com/SXZps2O71dTmOTpu)

接下來進入 mygeartest2
如圖所示，輸入第二齒所要的顏色跟數據 
Gear(midx, midy, rp, n=20, pa=20, color="black"):
第2齒輪齒數
n_g2 = '''+str(N1)+'''
![](https://copy.com/bU9yiSYZ2PVSPlTh)

寫出計算第二齒輪的節圓半徑
rp_g2 = m*n_g2/2
第2齒輪的圓心座標
x_g2 = x_g1 + rp_g1 + rp_g2
y_g2 = y_g1
x=第一齒的圓心座標+第一齒的節圓半徑+第二齒的節圓半徑
y=y軸不變所以跟齒輪一一樣
![](https://copy.com/Dfw4ng8rtaRki14R)

如下圖所示，接下來在第一齒角度後面輸入
 將第2齒輪逆時鐘轉 90 度之後, 再多轉一齒, 以便與第1齒輪進行囓合
ctx.save()
 translate to the origin of second gear
ctx.translate(x_g2, y_g2)
 rotate to engage
ctx.rotate(-pi/2-pi/n_g2)
 put it back
ctx.translate(-x_g2, -y_g2)
spur.Spur(ctx).Gear(x_g2, y_g2, rp_g2, n_g2, pa, "black")
ctx.restore()
![](https://copy.com/vdGQ9ucqYNFkOCF0)

以下就是完成的七齒輪嚙合圖!
![](https://copy.com/VFQKXMWXznSOZMxV)

# 由 scrum_1 組員40223102所寫的七齒輪嚙合考試報告
這次我負責的地方是個齒輪嚙合中，第四個齒輪和前面三個齒輪嚙合的部分。

在idexopy.com/fmGAv2sX2YTPF9yA)增加一行
第4齒數:input type=text name=N3 <br /
![](https://copy.com/FArtiR08qp3ubKc3)

之後到 mygeartest2
齒輪繪圖的部分增加第四個齒輪的定義 n_g4 = '''+str(N3)+'''
![](https://copy.com/fmGAv2sX2YTPF9yA)
第四個齒輪的節圓半徑 rp_g4 = m*n_g4/2，
還有定義第四個齒輪的圓心座標 
x_g4 = x_g1 + rp_g1 + 2*rp_g2 + 2* rp_g3 + rp_g4
y_g4 = y_g1
![](https://copy.com/EPDtDxLsszELM0qy)

然後是第四個齒輪和前面齒輪嚙合所需要轉的角度，
一開始第四齒先逆轉90度，再多加一齒，
第三顆齒輪跟第四可齒輪嚙合時會帶動第三齒轉一個角度，所以要再多加一個角度然後乘上第三第四齒的減速比，
第三齒轉動時會再帶動第二齒轉動，所以在減掉一個角度然後乘上第二第四齒的減速比。
![](https://copy.com/KkexdAbUaUze9CUa)