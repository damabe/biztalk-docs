---
title: "Warning - Custom Extension XML But No Custom XSLT | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""
ms.service: "biztalk-server"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bts10.map.warning.customExtensionXmlButNoCustomXSLT"
ms.assetid: 3219c73c-2e58-4fe2-bc6e-2d60348d2415
caps.latest.revision: 5
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Warning - Custom Extension XML But No Custom XSLT
**Error Code**  
  
 btm1033  
  
 **Explanation**  
  
 The **Custom Extension XML** property has been overridden without the **Custom XSLT Path** property being overridden. If this is intentional, you can ignore this warning.  
  
 BizTalk Mapper will use the XSLT produced by compiling the map and will also generate the Extension XML and append it to the custom Extension XML specified by the overridden property. This can be useful when the map contains **Scripting** functoids that use inline XSLT or inline XSLT call templates that make calls to one or more methods in external assemblies. In such cases, the user can then specify the prefix to assembly name mapping in the **Custom Extension XML** property.  
  
 **User Action**  
  
 If the condition indicated by this warning was not intentional, either provide a compatible value for the **Custom XSLT Path** property or remove the override value for the **Custom Extension XML** property.