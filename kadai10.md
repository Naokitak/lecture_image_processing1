% 課題10 画像のエッジ抽出 
% 次のプログラムを参考にして，エッジ抽出を体験せよ．
% 各自，Lenna以外の画像を用いよ． 
% 例

ORG = imread('cat.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); %カラーからグレイへの変換
imagesc(ORG); colormap('gray'); colorbar;% 画像表示
pause; % 一時停止
![原画像](https://github.com/Naokitak/lecture_image_processing/blob/master/10.1.png?raw=true)
図１：

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
pause; % 一時停止
![原画像](https://github.com/Naokitak/lecture_image_processing/blob/master/10.2.png?raw=true)
図2：

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
pause; % 一時停止
![原画像](https://github.com/Naokitak/lecture_image_processing/blob/master/10.3.png?raw=true)
図3：

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）
imagesc(IMG); colormap('gray'); colorbar;% 画像表示
pause; % 一時停止
![原画像](https://github.com/Naokitak/lecture_image_processing/blob/master/10.4.png?raw=true)
図4：


