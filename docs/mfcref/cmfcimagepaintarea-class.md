---
title: "CMFCImagePaintArea Class"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "CMFCImagePaintArea"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CMFCImagePaintArea class"
ms.assetid: c59eec22-f15a-4e58-8c4d-4a18a41f4452
caps.latest.revision: 17
ms.author: "mblome"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# CMFCImagePaintArea Class
Provides the picture area that you use to modify an image in an image editor dialog box.  
  
## Syntax  
  
```  
class CMFCImagePaintArea : public CButton  
```  
  
## Members  
  
### Public Constructors  
  
|||  
|-|-|  
|Name|Description|  
|[CMFCImagePaintArea::CMFCImagePaintArea](#cmfcimagepaintarea__cmfcimagepaintarea)|Constructs a `CMFCImagePaintArea` object.|  
|`CMFCImagePaintArea::~CMFCImagePaintArea`|Destructor.|  
  
### Public Methods  
  
|||  
|-|-|  
|Name|Description|  
|[CMFCImagePaintArea::GetMode](#cmfcimagepaintarea__getmode)|Retrieves the current drawing mode.|  
|[CMFCImagePaintArea::SetBitmap](#cmfcimagepaintarea__setbitmap)|Sets the bitmap image for the picture area.|  
|[CMFCImagePaintArea::SetColor](#cmfcimagepaintarea__setcolor)|Sets the current drawing color.|  
|[CMFCImagePaintArea::SetMode](#cmfcimagepaintarea__setmode)|Sets the current drawing mode.|  
  
### Remarks  
 This class is not intended to be used directly from your code.  
  
 The framework uses this class to display the picture area in an image editor dialog box. For more information about the image editor dialog box, see [CMFCImageEditorDialog Class](../mfcref/cmfcimageeditordialog-class.md).  
  
## Example  
 The following example demonstrates how to construct an object of the `CMFCImagePaintArea` class, set the current drawing color, set the current drawing mode, and set the bitmap image for the picture area.  
  
 [!code[NVC_MFC_RibbonApp#37](../mfcref/codesnippet/CPP/cmfcimagepaintarea-class_1.cpp)]  
  
## Inheritance Hierarchy  
 [CObject](../mfcref/cobject-class.md)  
  
 [CCmdTarget](../mfcref/ccmdtarget-class.md)  
  
 [CWnd](../mfcref/cwnd-class.md)  
  
 [CButton](../mfcref/cbutton-class.md)  
  
 [CMFCImagePaintArea](../mfcref/cmfcimagepaintarea-class.md)  
  
## Requirements  
 **Header:** afximagepaintarea.h  
  
##  <a name="cmfcimagepaintarea__cmfcimagepaintarea"></a>  CMFCImagePaintArea::CMFCImagePaintArea  
 Constructs a `CMFCImagePaintArea` object.  
  
```  
CMFCImagePaintArea( CMFCImageEditorDialog* pParentDlg );  
```  
  
### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pParentDlg`|A pointer to the dialog box that is the parent of the image editor.|  
  
##  <a name="cmfcimagepaintarea__getmode"></a>  CMFCImagePaintArea::GetMode  
 Retrieves the current drawing mode.  
  
```  
IMAGE_EDIT_MODE GetMode() const;  
```  
  
### Return Value  
 An `IMAGE_EDIT_MODE` value that specifies the current drawing mode.  
  
##  <a name="cmfcimagepaintarea__setbitmap"></a>  CMFCImagePaintArea::SetBitmap  
 Sets the bitmap image for the picture area.  
  
```  
void SetBitmap( CBitmap* pBitmap );  
```  
  
### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pBitmap`|The new bitmap image to display.|  
  
### Remarks  
 If `pBitmap` is `NULL`, this method sets the size of the modifiable paint area to zero. Otherwise, it sets the size of the modifiable paint area to the size of the provided bitmap image.  
  
##  <a name="cmfcimagepaintarea__setcolor"></a>  CMFCImagePaintArea::SetColor  
 Sets the current drawing color.  
  
```  
void SetColor( COLORREF color );  
```  
  
### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `color`|The new drawing color.|  
  
### Remarks  
 When you select a color from the image editor palette bar or color picker, the framework calls this method to update the current drawing color. The initial drawing color is black (a `COLORREF` value of 0).  
  
 The drawing color is used by the image editor dialog box for all drawing modes except for `IMAGE_EDIT_MODE_COLOR`. For more information about drawing modes, see [CMFCImagePaintArea::IMAGE_EDIT_MODE Enumeration](../mfcref/cmfcimagepaintarea--image_edit_mode-enumeration.md).  
  
##  <a name="cmfcimagepaintarea__setmode"></a>  CMFCImagePaintArea::SetMode  
 Sets the current drawing mode.  
  
```  
void SetMode(IMAGE_EDIT_MODE mode);  
```  
  
### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `mode`|An `IMAGE_EDIT_MODE` value that specifies the current drawing mode.|  
  
## See Also  
 [Hierarchy Chart](../mfc/hierarchy-chart.md)   
 [Classes](../mfcref/mfc-classes.md)   
 [CMFCImageEditorDialog Class](../mfcref/cmfcimageeditordialog-class.md)