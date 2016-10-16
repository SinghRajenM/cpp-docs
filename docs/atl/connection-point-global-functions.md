---
title: "Connection Point Global Functions"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "connection points [C++], global functions"
ms.assetid: bcb4bf50-2155-4e20-b8bb-f2908b03a6e7
caps.latest.revision: 15
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
# Connection Point Global Functions
These functions provide support for connection points and sink maps.  
  
> [!IMPORTANT]
>  The functions listed in the following table cannot be used in applications that execute in the [!INCLUDE[wrt](../atl/includes/wrt_md.md)].  
  
|||  
|-|-|  
|[AtlAdvise](../Topic/AtlAdvise.md)|Creates a connection between an object's connection point and a client's sink.|  
|[AtlUnadvise](../Topic/AtlUnadvise.md)|Terminates the connection established through `AtlAdvise`.|  
|[AtlAdviseSinkMap](../Topic/AtlAdviseSinkMap.md)|Advises or unadvises entries in an event sink map.|  
  
##  <a name="atladvise"></a>  AtlAdvise  
 Creates a connection between an object's connection point and a client's sink.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../atl/includes/wrt_md.md)].  
  
```
HRESULT     AtlAdvise(
    IUnknown*  pUnkCP,
    IUnknown*  pUnk,
    const IID& iid,
    LPDWORD pdw);
```  
  
### Parameters  
 `pUnkCP`  
 [in] A pointer to the **IUnknown** of the object the client wants to connect with.  
  
 *pUnk*  
 [in] A pointer to the client's **IUnknown**.  
  
 `iid`  
 [in] The GUID of the connection point. Typically, this is the same as the outgoing interface managed by the connection point.  
  
 `pdw`  
 [out] A pointer to the cookie that uniquely identifies the connection.  
  
### Return Value  
 A standard HRESULT value.  
  
### Remarks  
 The sink implements the outgoing interface supported by the connection point. The client uses the `pdw` cookie to remove the connection by passing it to [AtlUnadvise](../Topic/AtlUnadvise.md).  
  
### Example  
 [!code[NVC_ATL_Windowing#91](../atl/codesnippet/CPP/connection-point-global-functions_1.cpp)]  
  
##  <a name="atlunadvise"></a>  AtlUnadvise  
 Terminates the connection established through [AtlAdvise](../Topic/AtlAdvise.md).  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../atl/includes/wrt_md.md)].  
  
```
HRESULT     AtlUnadvise(
    IUnknown*  pUnkCP,
    const IID& iid,
    DWORD dw);
```  
  
### Parameters  
 `pUnkCP`  
 [in] A pointer to the **IUnknown** of the object that the client is connected with.  
  
 `iid`  
 [in] The GUID of the connection point. Typically, this is the same as the outgoing interface managed by the connection point.  
  
 `dw`  
 [in] The cookie that uniquely identifies the connection.  
  
### Return Value  
 A standard HRESULT value.  
  
### Example  
 [!code[NVC_ATL_Windowing#96](../atl/codesnippet/CPP/connection-point-global-functions_2.cpp)]  
  
##  <a name="atladvisesinkmap"></a>  AtlAdviseSinkMap  
 Call this function to advise or unadvise all entries in the object's sink event map.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../atl/includes/wrt_md.md)].  
  
```
HRESULT AtlAdviseSinkMap(
    T*  pT,  bool bAdvise);
```  
  
### Parameters  
 *pT*  
 [in] A pointer to the object containing the sink map.  
  
 `bAdvise`  
 [in] **true** if all sink entries are to be advised; **false** if all sink entries are to be unadvised.  
  
### Return Value  
 A standard HRESULT value.  
  
### Example  
 [!code[NVC_ATL_Windowing#92](../atl/codesnippet/CPP/connection-point-global-functions_3.h)]  
  
## See Also  
 [Functions](../atl/atl-functions.md)   
 [Connection Point Macros](../atl/connection-point-macros.md)
