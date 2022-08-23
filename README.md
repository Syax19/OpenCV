# OpenCV

* 成品影片連結：
> https://www.youtube.com/watch?v=gQS0T5kGlis

* Step 1:
> 使用Pytube.ipynb下載想做效果的YouTube影片(請注意版權問題)
1. 將link改成欲下載影片的YouTube網址
2. download()參數填入下載檔案存檔路徑


* Step 2:
> 使用OpenCV_FootageProcessing.ipynb做影片處理
1. cv2.VideoCapture()參數改為欲讀取檔案路徑
2. 如欲增加特效, 可更改seg_count = F_Count/n ; n為想將影片分為幾個片段做特效處理
3. 增加特效在if/elif/else條件判斷式之下
4. 若不增加特效, 本程式提供11種效果: 
> * 色彩轉換: BGR2RBG
> * 色彩轉換: BGR2HSV
> * CNN影像銳利化: Sharpen
> * 影像翻轉及疊加: Flip and 2 images addWeighted
> * 邊緣偵測: Sobel
> * 邊緣偵測: Canny
> * 邊緣偵測: Laplacian
> * 影像旋轉: Rotation
> * 利用背景提取繪製物體輪廓及偵測框: Draw contours and rectangle by MOG2
> * 型態梯度圖獲取圖片輪廓: Gradient
> * 特徵擷取: SIFT

* Step 3:
> 使用TakePictureManually.ipynb將影片截圖
1. cv2.VideoCapture()參數改為欲讀取檔案路徑
2. cv2.imwrite(f'./frame{count}.jpg', frame) 參數1為截圖存取路徑+檔名+檔案類型, 參數2為讀取的frame
