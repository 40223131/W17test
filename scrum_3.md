# 由 scrum_3 組員40223107所寫的七齒輪嚙合考試報告
我負責的地方是七個齒輪嚙合中，第三齒輪的部分。
首先開啟ger.leo →進入index 
在第二齒輪下方打上第3齒數:input type=text name=N3   br /
接下來進入 mygeartest2
輸入第三齒所要的顏色跟數據 
Gear(midx, midy, rp, n=20, pa=20, color="red"):

![](https://copy.com/cVlVzkV8lX4xBpHm)
第3齒輪齒數
n_g3 = '''+str(N2)+'''
寫出計算第三齒輪的節圓半徑
rp_g3 = m*n_g3/2

![](https://copy.com/OnFHCSro81yt62Fy)
第3齒輪的圓心座標
x_g3 = x_g1+ rp_g1 + rp_g2 +rp_g2 + rp_g3
y_g3 = y_g2
x=第一齒的圓心座標+第一齒的節圓半徑+第二齒的節圓半徑+第二齒的節圓半徑+第三齒的節圓半徑
水平軸不變Y=Y
接下來在第三齒角度後面輸入


將第3齒輪逆時鐘轉 90 度之後, 再多轉一齒, 以便與第2齒輪進行囓合
ctx.save()

 translate to the origin of second gear
ctx.translate(x_g3, y_g3)

rotate to engage
ctx.rotate(-pi/2-pi/n_g3)

put it back
ctx.translate(-x_g3, -y_g3)
spur.Spur(ctx).Gear(x_g3, y_g3, rp_g3, n_g3, pa, "red")
ctx.restore()
![](https://copy.com/xkRGGhCgiFM386EA)
好了之後save檔案，上傳到近端測試結果沒問題後，接下來上傳到github後完成

![](https://copy.com/VFQKXMWXznSOZMxV)


# 由 scrum_3 組員40223107所寫專案一考試報告
模數的基本公式是“節圓直徑/齒數=模數”
那我們先將節圓半徑*2/齒數可以就得到模數，兩個齒輪要互相嚙合必須要有一樣的模數，我們將其中一個節圓直徑*2，齒數也會跟著增加2倍，於是約分後得到的模數還是相同，還是可以嚙合。