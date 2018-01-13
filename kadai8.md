% 課題８ ラベリング
% 二値化された画像の連結成分にラベルをつけよ．
% 下記はサンプルプログラムである． 
% 課題作成にあたっては「Lenna」以外の画像を用いよ． 
% 例

ORG = imread('cat.jpg'); % 画像の読み込み
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/8.1.png?raw=true)
図１：

IMG = ORG > 128; % 閾値128で二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/8.2.png?raw=true)
図2：

IMG = bwlabeln(IMG);
imagesc(IMG); colormap(jet); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/8.3.png?raw=true)
図3：
