---
title: "ICommandImpl::m_bIsExecuting | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-data"]
ms.topic: "reference"
f1_keywords: ["ICommandImpl.m_bIsExecuting", "ATL::ICommandImpl::m_bIsExecuting", "m_bIsExecuting", "ATL.ICommandImpl.m_bIsExecuting", "ICommandImpl::m_bIsExecuting"]
dev_langs: ["C++"]
helpviewer_keywords: ["m_bIsExecuting"]
ms.assetid: 1e152164-514c-4116-88a3-16984af99991
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "data-storage"]
---
# ICommandImpl::m_bIsExecuting
Indicates whether the command is currently executing.  
  
## Syntax  
  
```cpp
unsigned m_bIsExecuting:1;  
  
```  
  
## Remarks  
 The **Execute** method of your command class can set this variable to **true**.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ICommandImpl Class](../../data/oledb/icommandimpl-class.md)   
 [ICommandImpl::m_bCancelWhenExecuting](../../data/oledb/icommandimpl-m-bcancelwhenexecuting.md)