# 2019CVFX_Homework6_Team5

## Original Videos
#### Video 1
<a href="https://youtu.be/E0rl5OCEfeA" target="_blank"><img src="./Images/original-video.png" alt="Original Video" width="240" height="180" border="10"/></a>

## ORB-SLAM2 vs 威力導演
<a href="https://youtu.be/fUQH25Jx-8Y" target="_blank"><img src="./Images/ORB-SLAM2.png" alt="ORB-SLAM2" width="240" height="180" border="10"/></a>
<a href="https://youtu.be/dsKpcQfdGlA" target="_blank"><img src="./Images/power.png" alt="Power" width="240" height="180" border="10"/></a>
<a href="https://youtu.be/35lXNmTyoq8" target="_blank"><img src="./Images/track.png" alt="Power" width="240" height="180" border="10"/></a>

### ORB-SLAM2
ORB-SLAM2 能夠提取圖片的特徵並做 pose estimation。我們對提供的 ros 範例中的monoAR 進行修改，讓他能夠放入我們想要的 model 以及文字。<br>

#### Insert 3D model
在 insert OBJ 的時候會依趙所計算出來的 map 去做 plane 的 detection，如果找得到的話則可以將 obj 插入 plane 的位置。
由於這份 code 所使用的 opengl 版本比較舊，並且插入方塊的部分並非 pipeline 的方式，所以我上網找了 GLM，利用他所提供的  glmDraw(GLMmodel* model, GLuint mode) 就可以順利的將 OBJ 檔 load 進去，缺點是無法貼上 texture。為了讓立體的效果可以看得出來，我們還加了 lightening 的效果，讓 obj 產生立體感。最後在播放的時候，plane 會根據每個 frame 的 pose 進行移動，而我們所加入的 obj 則會跟著 plane 進行移動，達到 match moving 的效果。

### 威力導演
利用威力導演中的 track motion 的功能，我們可以匡出我們想要 track 的部分，接下來他就會對匡選的部分進行 tracking。


## After Effects


