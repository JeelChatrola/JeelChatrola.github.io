---
layout: page
title: Chess Playing AI
description: 
img: assets/img/Chess.gif
importance: 4
category: work
related_publications:
---

Developed an interface of playing chess using Stockfish engine and Computer Vision in real world. Human vs AI (Stockfish engine).

Camera captures the image of chessboard then the image is analyzed using imageprocessing to identify the moves made by opponent and stockfish engine calculates the best possible move.

![opencv](https://img.shields.io/badge/CV-Open--CV-green) ![python](https://img.shields.io/badge/Py-Python3-blue)

## Youtube Video
[![check out my youtube video](https://img.youtube.com/vi/v12ELMNIZVE/0.jpg)](https://www.youtube.com/watch?v=v12ELMNIZVE)

## Method of Working
### Step - 1
Image1 : Image of Chess Board befor player move piece|Image2 : Image of Chess Board after player move piece
<table>
    <tr>
        <td valign="top" width="33%"><img src="/assets/img/projects/project_4/Step1_1.jpg" height="400" width="400"/></td>
        <td valign="top" width="33%"><img src="/assets/img/projects/project_4/Step1_2.jpg" height="400" width="400"/></td>
    </tr>
</table>
![](Method_working/Images/2.jpg)|![](Method_working/Images/3.jpg)

### Step - 2

<table>
    <tr>
        <td valign="top" width="33%">Difference of image by using function absdiff in CV2</td>
        <td valign="top" width="33%">Change Difference_image to Gray scale image</td>
    </tr>
    <tr>
    <td valign="top" width="33%">diff = cv2.absdiff(image1,image2) </td>
    <td valign="top" width="33%">diff_gray = cv2.cvtColor(diff,cv2.COLOR_BGR2GRAY)</td>
    </tr>
    <tr>
    <td valign="top" width="33%"><img src="/assets/img/projects/project_4/Step2_1.jpg" height="400" width="400"/>
    </td>
    <td valign="top" width="33%"><img src="/assets/img/projects/project_4/Step2_2.jpg" height="400" width="400"/></td>
    </tr>

</table>

### Step - 3

<table>
    <tr>
        <td valign="top" width="33%">Apply thresholding on Grayscale image</td>
        <td valign="top" width="33%">Find Contours on threshold image</td>
    </tr>
    <tr>
    <td valign="top" width="33%">matrix,thresold = cv2.threshold(diff_gray,value,255,cv2.THRESH_BINARY) </td>
    <td valign="top" width="33%">cnts,_ = cv2.findContours(thresold, cv2.RETR_EXTERNAL,cv2.CHAIN_APPROX_SIMPLE)</td>
    </tr>
    <tr>
    <td valign="top" width="33%"><img src="/assets/img/projects/project_4/Step3_1.jpg" height="400" width="400"/>
    </td>
    <td valign="top" width="33%"><img src="/assets/img/projects/project_4/Step3_2.jpg" height="400" width="400"/></td>
    </tr>

</table>