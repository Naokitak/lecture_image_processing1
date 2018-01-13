% 課題９ メディアンフィルタと先鋭化
% メディアンフィルターを適用し，ノイズ除去を体験せよ．
% 各自，Lenna以外の画像を用いよ．
% 例

ORG = imread('cat.jpg'); % 画像の読み込み
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/9.1.png?raw=true)
図１：

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付
imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/9.2.png?raw=true)
図2：

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/9.3.png?raw=true)
図3：

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/9.4.png?raw=true)
図4：

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計
IMG = filter2(f,IMG,'same'); % フィルタの適用
imagesc(IMG); colormap(gray); colorbar; % 画像の表示
pause;
![原画像](https://github.com/Naokitak/lecture_image_processing1/blob/master/9.5.png?raw=true)
図5：
