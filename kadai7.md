% 課題7　ダイナミックレンジの拡大
% 画素のダイナミックレンジを０から２５５にせよ． 
% 下記はサンプルプログラムである． 
% 課題作成にあたっては「Lenna」以外の画像を用いよ． 
% 例

ORG = imread('cat.jpg'); % 画像の読み込み
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/7.1.png?raw=true)
図１：

imhist(ORG); % 濃度ヒストグラムを生成、表示
pause;
ORG = double(ORG);
mn = min(ORG(:)); % 濃度値の最小値を算出
mx = max(ORG(:)); % 濃度値の最大値を算出
ORG = (ORG-mn)/(mx-mn)*255;
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/7.2.png?raw=true)
図2：

ORG = uint8(ORG); % この行について考察せよ
imhist(ORG); % 濃度ヒストグラムを生成、表示
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/7.3.png?raw=true)
図3：
