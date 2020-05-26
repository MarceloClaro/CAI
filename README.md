# CAI(Color Artificial Intelligence)
   
---
   
## [ About CAI Project ]
`CAI`�� ����ڰ� ���ε��� ������ ������ ���� �����Ͽ� �۽����÷� Ÿ���� �����ϰ�, �̸� ������� �۽����÷� �ȷ�Ʈ�� �м� �������� ��õ�մϴ�.   
������ ����� ���� ���� �ǴܵǾ��� �ְ����� �۽��� �÷� Ÿ���� ���� ������ ����ڿ��� �������� ������ ȭ��Ʈ �뷱�� ���� �� ��ó���� ���� ���� ���� ����� ������� �۽��� �÷� Ÿ���� �����մϴ�.   
   
`Personal Color`�� ���� ������ ��ü���� �ǹ��ϸ�, ������ Ư���� �м��Ͽ� �۽����÷� Ÿ�� �з�ü���� �� Ÿ�Կ� ������ �������� �׿� ��ȭ�� �̷�� ���� �����Ͽ� ������ ����ũ��, ���, �ǻ� ���� ��ä �̹����� �����ϴ� �ý����Դϴ�.   
   
#### `< CAI Total Process >`   
<img src="jay/img/total-process.jpg" width=100%>   
   
---
   
## [ Deep Learning_Personal Color Type Classifier ]
   
### Dataset Creater

#### `< Face Detection >`   
<img src="jay/img/face-detection.jpg" width=100%>   
   
#### `< Skin Color Extraction >`   
<img src="jay/img/skin-color-extraction.jpg" width=100%>   
   
#### `< Color System Converter & Type Classifier >`   
<img src="jay/img/color-system-converter.jpg" width=100%>   
   
- `Face Detection`   
	���ν�, �̹��� ������¡ (input image �� 20���� / output image �� 15����)   
	�ι� �̹����� ��ó�� �� `Haar Cascade`������� �� �ν�, ���ϵ� ������� �� �̹��� ȹ��   
- `Skin Color Extraction`   
	Face Detection���� ���� �� �̹������� �ȸ�� ����   
	������ ��Ȯ���� ���� 2���� ���� ���, K-means ����� �̿��� �� ����   
- `Color System Converter`   
	����� �� ����Ʈ�� ��� ������ ��ü �Ͽ� �˰��� ������ ���� �� ü�� ��ȯ   
	(BGR �� RGB �� HSV)   
- `Type Classifier`   
	�۽����÷� Ÿ�� �з� �˰����� ������ ���� ��� ��(�ȸ� ��)���� �����ͼ� ����   
   
   
### Deep Learning

#### `< CNN/AlexNet >`   
<img src="jay/img/cnn-alexnet.jpg" width=100%>   
   
`AlexNet` : ������ �κа� ������ �ƴ� �κ����� ������ ó���Ǳ� ������ '�� �н�'�� �����ϴٰ� �Ǵ��Ͽ� ����   
Result model : `CAI.h5`   
   
---
   
## [ Color Palette Extraction ]
   
### Bright Palette & Harmony Palette

#### `< Personal color Analysis >`   
<img src="jay/img/Data-Analysis.jpg" width=100%>   

�� �̷а� �۽����÷� ���� ���� �����Ͽ� 1�� ���� ���� & ���� �� ����   
�۽����÷� �̷а� ���� ���� & ���� ���� �ո����� �����ϱ� ���� �������� ����   
�ٰ��� �м��� ��Ȯ���� ���� ���̹� �����ͷ� �̿�, �м� Ȯ��   
�м� ����� ���� �۽����÷� Ÿ�� �з� ������ ���� ���� & ���� �� ����   
[* Personal color theory analysis report](https://github.com/slmteruto/CAI/blob/master/jay/Analysis/Report/Color_theory_analysis.ipynb)   
[* Personal color statistical analysis report](https://github.com/slmteruto/CAI/blob/master/cys/CAI_elementaryItem_analysis.ipynb)   
   
   
### Main purchase Palette

#### `< Data acquisition & Main color Extraction >`
<img src="jay/img/color-clustering.jpg" width=100%>   

- `Clothes color Extraction`   
	��ǰ �̹����� `Topwear.h5`(�мǾ����� �и� ��)�� �̿��� ����ũ ����   
	���� �̹����� ����ũ�� �����Ͽ� �мǾ������� ������ �̹��� ���� ����   
	K-means ����� �̿��� �� ����, ��ǰ �� �� �����͸� �����ͺ��̽��� ����   
- `Main color Extraction`   
	������� ���Ż�ǰ�� �ǽð����� ��ȸ, ������ ��ǰ�� �� ����Ʈ�� ȹ��   
	Gray tone Filter�� �̿��� ����Ʈ �� ��鿡 ������ ��ǰ�� ����   
	Ŭ�����͸��� ������ ������ ���� Color Generator�� ���Ż�ǰ ���� �Ը� Ȯ��   
	Ȯ��� �� �����͸� `Hierarchical Clustering`�� �̿��� �ֿ� ���� ���� �ȷ�Ʈ�� ����   
   
---
   
## [ Webstie ]

#### `< Web structure >`
<img src="jay/img/cai-webpage.jpg" width=100%>   

- `Personal color type Prediction`   
	���� ���� ����ڰ� ���ε��� ������ **CAI.h5**�� ����, �۽����÷� Ÿ���� ������ ����ڿ��� �ȳ�   
- `Matched Personal color palette`   
	������� Ÿ�� ����� **Skin Color Extraction**�� ������ �Ǻλ��� �����ϴ� ����ȭ �ȷ�Ʈ�� ����   
- `Fashion item Recommendation`   
	����� 3���� �ȷ�Ʈ�� �ش��ϴ� ��ǰ�� �����ͺ��̽����� �ǽð����� ��ȸ�� ��õ, ����ں� ����ȭ ���񽺸� ����   
	�� �ȷ�Ʈ1 : **Bright Palette** / �ȷ�Ʈ2 : **Harmony Palette** / �ȷ�Ʈ3 : **Main purchase Palette**   
[* Clustering accuracy evaluation report](https://github.com/slmteruto/CAI/blob/master/jay/Analysis/Report/Clustering_Evaluation.ipynb)   