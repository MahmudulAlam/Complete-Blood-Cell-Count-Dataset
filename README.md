# Complete Blood Cell Count Dataset
This is a modified version of blood cell count dataset. We have done some modification over the [original dataset](https://github.com/Shenggan/BCCD_Dataset/tree/master/BCCD). Three image annotation files show very low red blood cells (RBCs) than actual and one annotation file does not include any RBC although the blood cell image contains RBC. So, we clear up all four fallacious files and split the dataset into two parts: Training & Testing. First 300 blood cell images with annotations are used as training dataset and rest the 60s are used as testing dataset. The total dataset contains 360 blood smear images and their annotations.

[![Download](https://img.shields.io/badge/download-dataset-ff69b4.svg?style=flat)](https://github.com/MahmudulAlam/Complete-Blood-Cell-Count-Dataset/archive/master.zip)

## Ground Truth

### Image 

<p align="center">
  <img src="https://user-images.githubusercontent.com/37298971/46539603-c77ab900-c8d8-11e8-9e48-e6c054f8af3b.jpg" width="550">
</p>
N.B. Rectangular bounding boxes are converted to circular bounding boxes for representation.

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
