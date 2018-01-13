% 閾値を4パターン設定し,閾値処理た画像を示せ．
% 下記はサンプルプログラムである．
% 課題作成にあたっては「Lenna」以外の画像を用いよ．

clear; % 変数のオールクリア

ORG=imread('Lenna.png'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換


imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/3.1.png?raw=true)

図１：

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;
pause;


![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/3.2.png?raw=true)
図２：

IMG = ORG > 96;
imagesc(IMG); colormap(gray); colorbar;
pause;

![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/3.3.png?raw=true)
図3：


IMG = ORG > 128;
imagesc(IMG); colormap(gray); colorbar;
pause;

![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/3.4.png?raw=true)
図4：


IMG = ORG > 192;
imagesc(IMG); colormap(gray); colorbar;


![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/3.5.png?raw=true)

図5：
