---
title: "_variant_t::SetString"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "language-reference"
f1_keywords: 
  - "_variant_t::SetString"
  - "_variant_t.SetString"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "SetString method"
ms.assetid: 816b08e5-6830-46ca-b3d7-7689308b3be3
caps.latest.revision: 6
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
# _variant_t::SetString
**Microsoft Specific**  
  
 Assigns a string to this `_variant_t` object.  
  
## Syntax  
  
```  
  
      void SetString(  
   const char* pSrc   
);  
```  
  
#### Parameters  
 `pSrc`  
 Pointer to the character string.  
  
## Remarks  
 Converts an ANSI character string to a Unicode `BSTR` string and assigns it to this `_variant_t` object.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_variant_t Class](../cpp/_variant_t-class.md)