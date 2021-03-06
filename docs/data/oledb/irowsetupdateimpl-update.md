---
title: "IRowsetUpdateImpl::Update | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-data"]
ms.topic: "reference"
f1_keywords: ["ATL::IRowsetUpdateImpl::Update", "IRowsetUpdateImpl::Update", "IRowsetUpdateImpl.Update", "ATL.IRowsetUpdateImpl.Update"]
dev_langs: ["C++"]
helpviewer_keywords: ["Update method"]
ms.assetid: 9ec6884d-aa9c-4871-a803-c048f162403c
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "data-storage"]
---
# IRowsetUpdateImpl::Update
Transmits any changes made to the row since the last fetch or update.  
  
## Syntax  
  
```cpp
      STDMETHOD (Update )(HCHAPTER /* hReserved */,  
   DBCOUNTITEM cRows,  
   const HROW rghRows[],  
   DBCOUNTITEM* pcRows,  
   HROW** prgRows,  
   DBROWSTATUS** prgRowStatus);  
```  
  
#### Parameters  
 `hReserved`  
 [in] Corresponds to the `hChapter` parameter in [IRowsetUpdate::Update](https://msdn.microsoft.com/en-us/library/ms719709.aspx).  
  
 For other parameters, see [IRowsetUpdate::Update](https://msdn.microsoft.com/en-us/library/ms719709.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 Changes are transmitted by calling [IRowsetChangeImpl::FlushData](../../data/oledb/irowsetchangeimpl-flushdata.md). The consumer must call [CRowset::Update](../../data/oledb/crowset-update.md) for the changes to take effect. Set *prgRowstatus* to an appropriate value as described in [Row States](https://msdn.microsoft.com/en-us/library/ms722752.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetUpdateImpl Class](../../data/oledb/irowsetupdateimpl-class.md)