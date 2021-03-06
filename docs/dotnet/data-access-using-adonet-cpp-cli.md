---
title: "Data Access Using ADO.NET (C++/CLI) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-cli"]
ms.topic: "conceptual"
dev_langs: ["C++"]
helpviewer_keywords: ["ADO.NET [C++]", ".NET Framework [C++], data access", "databases [C++], accessing in C++", "data access [C++], ADO.NET", "data [C++], ADO.NET"]
ms.assetid: b0cd987d-1ea7-4f76-ba01-cbd52503d06d
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "dotnet"]
---
# Data Access Using ADO.NET (C++/CLI)
ADO.NET is the .NET Framework API for data access and provides power and ease of use unmatched by previous data access solutions. This section describes some of the issues involving ADO.NET that are unique to Visual C++ users, such as marshaling native types.  
  
 ADO.NET runs under the Common Language Runtime (CLR). Therefore, any application that interacts with ADO.NET must also target the CLR. However, that does not mean that native applications cannot use ADO.NET. These examples will demonstrate how to interact with an ADO.NET database from native code.  
  
## In This Section  
 [How to: Marshal ANSI Strings for ADO.NET (C++/CLI)](../dotnet/how-to-marshal-ansi-strings-for-adonet-cpp-cli.md)  
  
 [How to: Marshal BSTR Strings for ADO.NET (C++/CLI)](../dotnet/how-to-marshal-bstr-strings-for-adonet-cpp-cli.md)  
  
 [How to: Marshal Unicode Strings for ADO.NET (C++/CLI)](../dotnet/how-to-marshal-unicode-strings-for-adonet-cpp-cli.md)  
  
 [How to: Marshal a VARIANT for ADO.NET (C++/CLI)](../dotnet/how-to-marshal-a-variant-for-adonet-cpp-cli.md)  
  
 [How to: Marshal a SAFEARRAY for ADO.NET (C++/CLI)](../dotnet/how-to-marshal-a-safearray-for-adonet-cpp-cli.md)  
  
## Related Sections  
  
|Section|Description|  
|-------------|-----------------|  
|[ADO.NET](/dotnet/framework/data/adonet/index)|Provides an overview of ADO.NET, a set of classes that expose data access services to the .NET programmer.|  
  
## See Also  
 [.NET Programming with C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)   
 [Native and .NET Interoperability](../dotnet/native-and-dotnet-interoperability.md)