clear; % 変数のオールクリア
ORG=imread('cat.png'); % 原画像の入力
ORG = rgb2gray(ORG);
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause; % 一時停止
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/6.1.png?raw=true)
図１：

IMG = ORG>128; % 128による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/6.2.png?raw=true)
図2：
IMG = dither(ORG); % ディザ法による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/6.3.png?raw=true)
図3：
