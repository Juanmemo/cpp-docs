---
title: "Compiler Error C3280 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: ["cpp-tools"]
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: ["C3280"]
dev_langs: ["C++"]
helpviewer_keywords: ["C3280"]
ms.assetid: 86dc5bbc-8818-4786-a728-9334268d308b
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
ms.workload: ["cplusplus"]
---
# Compiler Error C3280
'class' : a member-function of a managed type cannot be compiled as an unmanaged function  
  
 Managed class member functions cannot be compiled as unmanaged functions.  
  
 The following sample generates C3280:  
  
```  
// C3280_2.cpp  
// compile with: /clr  
ref struct A {  
   void func();  
};  
  
#pragma managed(push,off)  
  
void A::func()   // C3280  
{  
}  
  
#pragma managed(pop)  
```  
