# 由 scrum_2 組員40223106所寫的專案一考試報告
: 大家很積極地詢問會編寫的同學，然後都編寫了一份.py檔案。
交給product-owner 再統一導入各 .py 檔案，並且繼續執行接下來的的協同2D繪圖工作。




# 由 scrum_2 組員40223106所寫的七齒輪嚙合考試報告
我們每個組員所負責的齒輪，如下圖:
![](https://copy.com/VFQKXMWXznSOZMxV)

我所負責的齒輪是第五顆齒輪。
需要修改的部分有，圓心座標、節圓半徑、轉動角度、壓力角、顏色跟數據。
齒輪轉角公式需要用到減速比。

要修改之前要從GITHUB上CLONE下來後，開啟gear.leo 後進入index。 
在第四齒輪下方打上第五齒數，
![](https://copy.com/DMjA1kh64AsIQpYP)
再接下來進入 "mygeartest2"
輸入第五齒所要的顏色跟數據 
Gear(x_g5,y_g5,rp_g5,n_g5,pa,"purple")

第五齒輪的公式為: -180/PI-齒寬+g5*g4減速比-g5*g3減速比-g5*g2減速比。