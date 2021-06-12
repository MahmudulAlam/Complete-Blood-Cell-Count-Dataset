<h2 align="center">Complete Blood Count (CBC) Dataset</h2>

[![GitHub stars](https://img.shields.io/github/stars/MahmudulAlam/Complete-Blood-Cell-Count-Dataset)](https://github.com/MahmudulAlam/Complete-Blood-Cell-Count-Dataset/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/MahmudulAlam/Complete-Blood-Cell-Count-Dataset)](https://github.com/MahmudulAlam/Complete-Blood-Cell-Count-Dataset/network)
[![GitHub issues](https://img.shields.io/github/issues/MahmudulAlam/Complete-Blood-Cell-Count-Dataset)](https://github.com/MahmudulAlam/Complete-Blood-Cell-Count-Dataset/issues)
[![GitHub license](https://img.shields.io/github/license/MahmudulAlam/Complete-Blood-Cell-Count-Dataset)](https://github.com/MahmudulAlam/Complete-Blood-Cell-Count-Dataset/blob/master/LICENSE)

The [```complete blood count (CBC)```](https://mahmudulalam.github.io/Complete-Blood-Cell-Count-Dataset/) dataset contains 360 blood smear images along with their annotation files splitting into ```Training```, ```Testing```, and ```Validation``` sets. The training folder contains 300 images with annotations. The testing and validation folder both contain 60 images with annotations. We have done some modification over the [```original dataset```](https://github.com/Shenggan/BCCD_Dataset/tree/master/BCCD) to prepare this CBC dataset where some of the image annotation files contain very low red blood cells (RBCs) than actual and one annotation file does not include any RBC at all although the cell smear image contains RBCs. So, we clear up all the fallacious files and split the dataset into three parts. Among the 360 smear images, 300 blood cell images with annotations are used as the training set first, and then the rest of the 60 images with annotations are used as the testing set. Due to the shortage of the data, a subset of the training set is used to prepare the validation set which contains 60 images with annotations.

[![Download](https://img.shields.io/badge/download-dataset-f20a0a.svg?longCache=true&style=flat)](https://github.com/MahmudulAlam/Complete-Blood-Cell-Count-Dataset/archive/master.zip)

## Paper 
[![Paper](https://img.shields.io/badge/paper-IETDigiLib-830ceb.svg?longCache=true&style=flat)](http://ietdl.org/t/kmgztb) [![Paper](https://img.shields.io/badge/paper-Wiley-282829.svg?longCache=true&style=flat)](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/htl.2018.5098)

The dataset is modified and prepared for this [```paper```](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/htl.2018.5098) for [```automatic identification and counting of blood cells```]( https://github.com/MahmudulAlam/Automatic-Identification-and-Counting-of-Blood-Cells):link: If you use this dataset, please cite this paper: 

[***```Machine learning approach of automatic identification and counting of blood cells```***](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/htl.2018.5098)

```
@article{alam2019machine,
  title={Machine learning approach of automatic identification and counting of blood cells},
  author={Alam, Mohammad Mahmudul and Islam, Mohammad Tariqul},
  journal={Healthcare Technology Letters},
  volume={6},
  number={4},
  pages={103--108},
  year={2019},
  publisher={IET}
}
```

## Data Description

### Image 
Each image is resized to ```640 x 480``` resolution. 
<p align="center">
  <img src="https://user-images.githubusercontent.com/37298971/46539603-c77ab900-c8d8-11e8-9e48-e6c054f8af3b.jpg" width="500">
</p>

`N.B.` Rectangular bounding boxes are converted to circular bounding boxes for representation.

### Annotation Format

```
 <annotation>
	<folder>JPEGImages</folder>
	<filename>BloodImage_00395.jpg</filename>
	<path>/home/pi/detection_dataset/JPEGImages/BloodImage_00395.jpg</path>
	<source>
		<database>Unknown</database>
	</source>
	<size>
		<width>640</width>
		<height>480</height>
		<depth>3</depth>
	</size>
	<segmented>0</segmented>
	<object>
		<name>RBC</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<difficult>0</difficult>
		<bndbox>
			<xmin>25</xmin>
			<ymin>90</ymin>
			<xmax>127</xmax>
			<ymax>209</ymax>
		</bndbox>
	</object>
  . . . . . . . . 
  . . . . . . . . Rest of the RBC
  . . . . . . . . 
 	<object>
		<name>WBC</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<difficult>0</difficult>
		<bndbox>
			<xmin>114</xmin>
			<ymin>66</ymin>
			<xmax>351</xmax>
			<ymax>294</ymax>
		</bndbox>
	</object>
	<object>
		<name>Platelets</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<difficult>0</difficult>
		<bndbox>
			<xmin>472</xmin>
			<ymin>201</ymin>
			<xmax>540</xmax>
			<ymax>268</ymax>
		</bndbox>
	</object>
  . . . . . . . . 
  . . . . . . . . Rest of the platelets
  . . . . . . . . 
  </annotation>
```

[1]: http://ietdl.org/t/kmgztb
